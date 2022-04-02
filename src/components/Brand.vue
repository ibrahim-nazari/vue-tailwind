<template>
  <div class="container mx-auto">
    <div
      class="flex flex-col justify-center items-center md:items-start space-y-4 md:space-y-0 md:flex-row"
    >
      <div class="image-container relative min-h-[360px]  w-[200px] md:w-[350px]">
        <img
          :src="imageright"
          class="transition image-style ease-in-out delay-150 hover:translate-x-8 duration-1000 absolute -top-4 left-0 w-full"
        />
      </div>
      <div class="flex-1 flex flex-wrap items-center justify-center">
        <div
          @mouseover="active = item"
          @mouseleave="active = 100"
          v-for="item in 6"
          :key="item"
          :class="`${item % 2 == 0 ? 'bg-gray-800' : 'bg-gray-700'} ${
            active == item
              ? 'bg-[url(data:image/png;base64,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)]'
              : ''
          }`"
          class="p-5 w-[280px] h-[280px] flex items-center justify-center flex-col bg-no-repeat bg-cover"
        >
          <img :src="brandImage" class="w-28 mb-2" />
          <h4 class="text-3xl my-2 uppercase text-gray-400">ae live</h4>
          <h4 class="text-xl my-2 text-gray-400">Live casino</h4>
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
      brandImage: require("../assets/images/brand.png"),
      imageright: require("../assets/images/brandsideimage.png"),
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

.image-style{
    max-height: 590px;
}
</style>
