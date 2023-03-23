<template>
  <NavBar />
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="4" lg="4" sm="4">
        <div class="filters text-center mb-3">
          <!-- SHOW ALL BUTTON -->
          <!-- FILTER BUTTONS -->
          <div
            class="p-3 bg-orange"
            style="overflow: auto; white-space: nowrap"
          >
            <v-btn class="mb-3" @click="showAll()"> الكل </v-btn>
            <ul>
              <li v-for="(cat, index) in cats" :key="index">
                <v-btn class="my-3" @click="filterArticle(cat)" width="168">
                  <v-icon color="orange-accent-4" :icon="cat.icon" />
                  {{ cat.name }}
                </v-btn>
              </li>
            </ul>
          </div>
        </div>
      </v-col>
      <v-col cols="12" md="8" lg="8" sm="8" class="bg-red">
        <div>
          <!-- FILTER BUTTONS -->
          <!-- products -->
          <div class="row d-flex justify-content-center">
            <v-row justify="center" align="center">
              <v-col
                cols="12"
                lg="3"
                md="6"
                v-for="item in filterapps"
                :key="item.id"
              >
                <div>
                  <div class="card rounded-xl graphics_img">
                    <div class="images" v-viewer.static="{ title: false }">
                      <img
                        :src="item.image"
                        height="200"
                        title="false"
                        style="width: 100%"
                      />
                    </div>
                  </div>
                </div>
              </v-col>
            </v-row>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import NavBar from "../components/NavBar.vue";
export default {
  components: {
    NavBar,
  },
  name: "GraphicCom",
  data() {
    return {
      filteredCat: null,
      cats: [
        { id: 1, name: "اختيار الخدمة", icon: "mdi:mdi-account-star" },
        { id: 2, name: "التاريخ والوقت", icon: "mdi:mdi-calendar-range" },
        { id: 3, name: "تفاصيل اساسية", icon: "mdi:mdi-details" },
        { id: 4, name: "البيانات الشخصية", icon: "mdi:mdi-data-matrix" },
      ],
      products: [
        {
          id: 1,
          cat_id: 1,
          image:
            "https://img.freepik.com/free-photo/close-up-young-adult-enjoying-warm-drink_23-2149134373.jpg?w=740&t=st=1672488370~exp=1672488970~hmac=87f604c13d559be68b0c9a47f1ba4e7b0b87d3d7e31904b9ba02e3e4adff2cd1",
        },
        {
          id: 2,
          cat_id: 2,
          image:
            "https://img.freepik.com/free-photo/close-up-young-adult-enjoying-warm-drink_23-2149134373.jpg?w=740&t=st=1672488370~exp=1672488970~hmac=87f604c13d559be68b0c9a47f1ba4e7b0b87d3d7e31904b9ba02e3e4adff2cd1",
        },
        {
          id: 3,
          cat_id: 2,
          image:
            "https://img.freepik.com/free-vector/cartoon-web-design-landing-page_52683-70880.jpg?w=900&t=st=1672497244~exp=1672497844~hmac=5d3ac2cf1dae973a4aa1010048251ffad4cf8e93ab9aac128d8a14fa08b0ea91",
        },
        {
          id: 4,
          cat_id: 2,
          image:
            "https://img.freepik.com/free-vector/minimalist-background-gradient-design-style_483537-2988.jpg?w=826&t=st=1672497292~exp=1672497892~hmac=5dde22047d413f18ad76e2a13d28cce4050575c86be4749f1b0d479a2c067d87",
        },
        {
          id: 5,
          cat_id: 3,
          image:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Adobe_Illustrator_CC_icon.svg/512px-Adobe_Illustrator_CC_icon.svg.png",
        },
        {
          id: 6,
          cat_id: 3,
          image:
            "https://img.freepik.com/free-vector/tiny-graphic-designer-drawing-with-big-pen-computer-screen-creators-work-creative-woman-working-laptop-flat-vector-illustration-digital-design-concept-banner-landing-web-page_74855-25342.jpg?w=740&t=st=1672497393~exp=1672497993~hmac=3b0286ad7b29f8baa045d3d141cc46745afec9bcc567f5df2f8a8e13641d84a5",
        },
      ],
    };
  },
  methods: {
    filterArticle(cat) {
      // Set filteredCat data to
      // selected product's name
      this.filteredCat = cat.id;
    },
    // set filteredCat data to null
    showAll() {
      this.filteredCat = null;
    },
  },
  computed: {
    // When filteredCat data changed
    // filterapps computed property will
    // automatically create new data model
    // by filtering out unmatched products
    filterapps() {
      // If filteredCat is equal to null
      // display all data
      const data = this.filteredCat
        ? this.products.filter((item) => item.cat_id === this.filteredCat)
        : this.products;
      return data;
    },
  },
};
</script>

<style scoped>
* {
  direction: rtl;
}
</style>
