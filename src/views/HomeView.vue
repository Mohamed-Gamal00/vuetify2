<template>
  <NavBar />
  <div>
    <h1 class="text-center">home</h1>
  </div>
</template>

<script>
import { defineComponent } from "vue";

// Components
import NavBar from "../components/NavBar.vue";

export default defineComponent({
  name: "HomeView",
  components: {
    NavBar,
  },
  setup() {
    return {};
  },
});
</script>
<style scoped></style>
