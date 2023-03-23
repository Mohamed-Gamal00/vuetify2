<template>
  <div class="about">
    <v-container fluid>
      <!-- section1 -->
      <v-row align="center" justify="center" style="height: 100%">
        <v-col cols="10">
          <v-row align="center">
            <v-col cols="12" lg="6" md="6" sm="6">
              <div class="text-black" style="direction: rtl">
                <p class="font-weight-bold myorange cairo">مركز العسقلاني</p>
                <!-- <v-card-title class="text-h6 text-md-h1 text-lg-h4">Title</v-card-title> -->
                <h1
                  class="lh-5 text-h5 font-weight-bold text-md-h5 text-lg-h4 marai"
                >
                  مركز العسقلاني لطب الأسنان
                </h1>
                <p class="font-weight-bold">
                  احصل علي ابستامه مشرقة وصحية بمركز العسقلاني لطب الاسنان,
                  معالجة الأسنان ب احدث التقنيات, تخلص من مشاكل الاسنان.
                </p>
                <v-btn class="bg-myorange text-white mt-3 font-weight-bold">
                  <v-icon
                    color="grey-lighten-3"
                    icon="mdi:mdi-arrow-left-circle"
                  />

                  احجز موعد
                </v-btn>
              </div>
            </v-col>
            <v-col cols="12" lg="6" md="6" sm="6" align="center">
              <div>
                <v-img cover src="@/assets/images/img.webp" />
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <!-- section2 -->
      <v-row
        class="mt-lg-12"
        align="center"
        justify="center"
        style="height: 100%"
      >
        <v-col cols="10">
          <v-row align="center">
            <v-col cols="12" lg="6" md="6" sm="6" align="center">
              <div>
                <v-img
                  width="388px"
                  class="rounded-xl"
                  cover
                  src="@/assets/images/png.png"
                />
              </div>
            </v-col>
            <v-col
              class="rounded-xl"
              cols="12"
              lg="6"
              md="6"
              sm="6"
              style="background-color: #faf9f9"
            >
              <div class="text-black my-lg-4" style="direction: rtl">
                <p class="font-weight-bold myorange cairo">مركز العسقلاني</p>
                <!-- <v-card-title class="text-h6 text-md-h1 text-lg-h4">Title</v-card-title> -->
                <h1
                  class="lh-5 text-h5 font-weight-bold text-md-h5 text-lg-h4 marai"
                >
                  مركز العسقلاني لطب الأسنان
                </h1>
                <p class="font-weight-bold">
                  فريق كامل من أفضل الأطباء وفي كل المجالات التي تخدم مجال طب
                  جراحة الفم والأسنان, متخصصون في زراعة الأسنان, التقويم, تجميل
                  الأسنان.
                </p>
                <v-btn class="bg-myorange text-white mt-3 font-weight-bold">
                  <v-icon
                    color="grey-lighten-3"
                    icon="mdi:mdi-arrow-left-circle"
                  />

                  احجز موعد
                </v-btn>
              </div>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <!-- section3 -->
      <v-row
        class="mt-lg-12"
        align="center"
        justify="center"
        style="height: 100%"
      >
        <v-col cols="10">
          <v-row align="center">
            <v-col
              cols="12"
              lg="4"
              md="6"
              sm="6"
              align="center"
              v-for="card in cards"
              :key="card.id"
            >
              <v-card class="mx-auto" max-width="272" height="169">
                <v-card-item class="text-center">
                  <div>
                    <v-btn
                      height="60"
                      style="border-radius: 16px"
                      class="my-5"
                      color="orange-lighten-5"
                      icon="mdi:mdi-monitor-cellphone-star"
                      size="x-large"
                    >
                      <v-icon color="orange-accent-4" :icon="card.icon" />
                    </v-btn>
                    <div class="mb-1">
                      <p class="fs-15 text-blue-grey-darken">
                        {{ card.title }}
                      </p>
                    </div>
                  </div>
                </v-card-item>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <!-- section4 -->
      <v-row
        class="mt-lg-12"
        justify="center"
        style="background-color: #faf9f9"
      >
        <div class="text-center mt-lg-5">
          <h6 class="myorange fs-18 lh-2">مواعيد العمل</h6>
          <h4 class="lh-2 text-h5 marai my-3 font-weight-bold">تعرف علي مواعيد العمل والخدمات المتاحة</h4>
          <p class="fs-14 lh-2">من الساعة 12 ظهرا حتى الساعة 11 مساءا (بحجز مسبق)</p>
          <p class="fs-14">
            الجمعة: من الساعة 4 مساءا حتى الساعة 9 مساءا (بحجز مسبق)
          </p>
        </div>
      </v-row>
    </v-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cards: [
        {
          title: "جودة وكفاة من فريق الأطباء للوصول الي اعلى درجات الرضى.",
          icon: "mdi:mdi-monitor-cellphone-star",
          flex: 12,
        },
        {
          title:
            "فريق كامل من الأطباء والممرضين للوصول بالخدمة الي اعلى مستوى.",
          icon: "mdi:mdi-account-group",
          flex: 6,
        },
        {
          title: "اطباء علي اعلى مستوى من الكفاءه.",
          icon: "mdi:mdi-trending-up",
          flex: 6,
        },
      ],
    };
  },
};
</script>
<style scoped>
* {
  direction: rtl;
}
.v-btn {
  border-radius: 20px;
  height: 40px;
}
/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .lh-5 {
    line-height: 5rem !important;
  }
  .lh-3 {
    line-height: 3rem !important;
  }
  .lh-2 {
    line-height: 2rem !important;
  }
}
</style>
