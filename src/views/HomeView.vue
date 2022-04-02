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
    <div class="game-type-container-custom my-12">
      <GameType />
    </div>
    <div class="game-type-container-custom my-12">
      <Brand />
    </div>
    <div class="game-type-container-custom my-12">
      <Footbal />
    </div>
    <div class="my-20"></div>
  </div>
</template>

<script>
// @ is an alias to /src
import CarouselComponent from "@/components/CarouselComponent.vue";
import SportCategory from "@/components/SportCategory.vue";
import GameType from "@/components/GameType.vue";
import Brand from "@/components/Brand.vue";
import Footbal from "@/components/Footbal.vue";

export default {
  name: "HomeView",
  components: {
    CarouselComponent,
    SportCategory,
    GameType,
    Brand,
    Footbal
  },
  data() {
    return {};
  },
  methods: {},
};
</script>

<style scope></style>
