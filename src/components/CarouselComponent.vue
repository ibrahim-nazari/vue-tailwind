<template>
  <carousel :autoplay="2000" :transition="800" :wrap-around="true">
    <slide class="h-[180px] sm:h-[220px] md:h-[280px] lg:h-[320px] xl:h-[350px]" v-for="(img, i) in images" :key="i">
      <img class="object-cover h-full w-full" :src="img" alt="First slide" />
    </slide>
    <template #addons>
      <Navigation />
      <Pagination />
  
    </template>
  </carousel>
</template>

<script>
import { Carousel, Slide, Pagination, Navigation } from "vue3-carousel";
export default {
  name: "CarouselComponent",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
      images: [
        require("../assets/images/slide1.jpg"),
        require("../assets/images/slide2.jpg"),
        require("../assets/images/slide3.jpg"),
        require("../assets/images/slide4.jpg"),
      ],
      active: 0,
    };
  },
};
</script>
<style>
.carousel__prev{
  left:26px !important;
}
.carousel__next{
  right:26px !important;
}

</style>
