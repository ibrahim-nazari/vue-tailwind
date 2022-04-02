<template>
  <div class="container mx-auto">
    <div
      class="relative max-h-[800px] flex justify-center items-center"
    >
      <div class="flex justify-between items-center flex-row sm:flex-col sm:h-full absolute top-0 left-1/2 translate-x-[-50%] sm:translate-x-16 sm:left-0">
        <div v-for="(img, i) in left" :key="i" class="relative w-[240px]">
          <img :src="img" :class="`w-full absolute ${i==1?'sm:bottom-0 xs:top-0':'top-0'} left-0`" />
        </div>
      </div>
      <div class="">
        <img :src="centerimage" class=" object-center object-contain" />
      </div>

      <div class="flex justify-between items-center flex-row sm:flex-col sm:h-full absolute bottom-0 sm:top-0 left-1/2 translate-x-[-50%] sm:translate-x-16 sm:right-0">
        <div v-for="(img, i) in right" :key="i" class="relative w-[240px]">
           <img :src="img" :class="`w-full absolute ${i==1?'sm:bottom-0 xs:top-0 ':'top-0'} left-0`" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Brand",
  components: {},
  data() {
    return {
      right: [
        require("../assets/images/footbal/circle1.png"),
        require("../assets/images/footbal/circle2.png"),
      ],
      left: [
        require("../assets/images/footbal/circle3.png"),
        require("../assets/images/footbal/circle3.png"),
      ],
      centerimage: require("../assets/images/footbal/center.png"),
      active: 100,
    };
  },
  methods: {},
};
</script>

<style scoped>
.container {
  max-width: 1200px;
}

.image-style {
  max-height: 590px;
}
</style>
