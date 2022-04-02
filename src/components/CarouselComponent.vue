<template>
  <carousel :autoplay="2000" :transition="800" :wrap-around="true">
    <slide class="h-[380px]" v-for="(img, i) in images" :key="i">
      <img class="object-cover h-full w-full" :src="img" alt="First slide" />
    </slide>
    <template #addons>
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
