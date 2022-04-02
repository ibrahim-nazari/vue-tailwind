<template>
  <div class="container mx-auto ">
    <div class="justify-items-center  grid grid-cols-1 md:grid-cols-2">
      <div class="left-section">
        <div
          @mouseover="active = i"
          v-for="(img, i) in images"
          :key="i"
          :class="`${active == i && 'bg-gray-800'}`"
          class="flex p-5 box-border  items-center space-x-3 w-[400px]"
        >
          <img :src="img" class="w-28" />
          <div>
            <h4 class="text-3xl uppercase italic">pt slot</h4>
            <p class="italic uppercase mt-3">e-game</p>
          </div>
        </div>
      </div>
      <div class="right-section flex flex-col justify-between items-center mt-10 md:mt-0">
          <img :src="imageright" class="h-[300px] md:h-[400px] lg:h-[550px]" />
          <div class=" text-center my-10">
               <button 
       class=" bg-[url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMoAAAAzCAMAAADhJmdLAAABIFBMVEUAAAAAAADmoCKiawTGggVdQQ1QNQLWkRTFggQSDADnoCLHhQfFgQTooSPmnyKWaBaBVQPnoCIVDgMRDALGgwbFgQS9gx29hBy9gxy9ghznoCPmoCLGgwYXEAPooSPFgQShbgDooSPnoSOkbgD/+oPIhwv/+YH+9HvKiQ6obgD77XP46G/kvkPgmh6+fQi5eQW0dgOwcwHjnR//93788Hj242rz3GLx2F7t0FXqy1DhuDzeszfaqy/YpSnUniHRmR3clxzZlRrWkhfOkhbSjxXOjBLMjBHCgQuldgiscAD14Gbv1Fnoxkznw0jDpjbcrzPWoiW3lCXQlhmviBnMkBKrgRLFhA2icQPu5XDOtkXLskHHrTy+ny+7miuzjh+ofA6gusWWAAAAH3RSTlOAAPPZvqCgG5aGVfTyvr69vZaGhVVV2dnZ2ZaWloZVGvIexgAAAT9JREFUaN7t2lV2AkEQheEePESBuBsJccHGXXEnnv3vIj3hcNhCTZ/6VtD/Qz/VJRzHbSaWi8ViqVRy3dHIsqzBQNM0VVV7PUVRZFnudiVJEkXxnmq3Wy1BEHiebzbr9XqtVms0qtXqHXVLVSqV61C5XL4KXf57e//47HS+vvv9n+FwPP71fX86PV24mLkJBUHwQj1TT9Qj5XneZBI+0HUcx7Zt0zQNw9B1/YF6pWJrWZpBuPRhPLVEIi2f3MmlaUpmgzBgfZ8jW3HChO1jkkgRJiRXyUrE/8ncUYycEEacYQpAmAIRpkCEKRBhCkSYAhGmQIQpEGEKRJgCEUMp55gCEKZAhCkQYQpEmAIRpkCEKRBhCkRMpbByt8/HWFpTsLJx2c0yszzKhXuwTDxVIJFWSO4dpLn5Si/SM73ZSu8PhT5giUJGXmAAAAAASUVORK5CYII=')] uppercase font-bold
        bg-[#1f2d3d1c] text-[#ebc86d] border 
       border-[#ebc86d] px-5 py-3
       w-[202px]
       italic
       ">Buy Now</button>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GameType",
  components: {},
  data() {
    return {
      images: [
        require("../assets/images/gametype/type1.png"),
        require("../assets/images/gametype/type2.png"),
        require("../assets/images/gametype/type3.png"),
        require("../assets/images/gametype/type4.png"),
      ],
      active: 0,
      imageright:require("../assets/images/gametype/typeright.png")
    };
  },
  methods: {},
};
</script>

<style scoped>
.container {
  max-width: 1200px;
}
</style>
