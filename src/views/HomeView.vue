<template>
  <div class="home">
    <header>
      <h3 class="text-3xl text-center my-10">Home</h3>
    </header>
    <div class="carousel-container-custom">
      <CarouselComponent />
    </div>
    <div class="card-container-custom my-8">
      <SportCategory />
    </div>
    <div class="my-20"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import CarouselComponent from "@/components/CarouselComponent.vue";
import SportCategory from "@/components/SportCategory.vue";

export default {
  name: "HomeView",
  components: {
    CarouselComponent,
    SportCategory,
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scope></style>
