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
                  class="lh text-h5 font-weight-bold text-md-h5 text-lg-h4 marai"
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
                  class="lh text-h5 font-weight-bold text-md-h5 text-lg-h4 marai"
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
      <v-row
        class="mt-lg-12"
        align="center"
        justify="center"
        style="height: 100%"
      >
        <v-col cols="10">
          <v-row align="center">
            <v-col cols="12" lg="6" md="6" sm="6" align="center">
              <v-card class="mx-auto" max-width="344" variant="outlined">
                <v-card-item>
                  <div>
                    <div class="text-overline mb-1">OVERLINE</div>
                    <div class="text-h6 mb-1">Headline</div>
                    <div class="text-caption">
                      Greyhound divisely hello coldly fonwderfully
                    </div>
                  </div>
                </v-card-item>

                <v-card-actions>
                  <v-btn variant="outlined"> Button </v-btn>
                </v-card-actions>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
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
  .lh {
    line-height: 5rem;
  }
}
</style>
