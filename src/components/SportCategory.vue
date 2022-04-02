<template>
<div class="container mx-auto ">
    <div class=" justify-items-center grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-10">
   <div v-for="(img,i) in images" :key="i" class="relative group  cursor-pointer h-[330px] w-[267px]">
       <img :src="img" class="w-full group-hover:opacity-60" />
       <button 
       class=" bg-[url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMoAAAAzCAMAAADhJmdLAAABIFBMVEUAAAAAAADmoCKiawTGggVdQQ1QNQLWkRTFggQSDADnoCLHhQfFgQTooSPmnyKWaBaBVQPnoCIVDgMRDALGgwbFgQS9gx29hBy9gxy9ghznoCPmoCLGgwYXEAPooSPFgQShbgDooSPnoSOkbgD/+oPIhwv/+YH+9HvKiQ6obgD77XP46G/kvkPgmh6+fQi5eQW0dgOwcwHjnR//93788Hj242rz3GLx2F7t0FXqy1DhuDzeszfaqy/YpSnUniHRmR3clxzZlRrWkhfOkhbSjxXOjBLMjBHCgQuldgiscAD14Gbv1Fnoxkznw0jDpjbcrzPWoiW3lCXQlhmviBnMkBKrgRLFhA2icQPu5XDOtkXLskHHrTy+ny+7miuzjh+ofA6gusWWAAAAH3RSTlOAAPPZvqCgG5aGVfTyvr69vZaGhVVV2dnZ2ZaWloZVGvIexgAAAT9JREFUaN7t2lV2AkEQheEePESBuBsJccHGXXEnnv3vIj3hcNhCTZ/6VtD/Qz/VJRzHbSaWi8ViqVRy3dHIsqzBQNM0VVV7PUVRZFnudiVJEkXxnmq3Wy1BEHiebzbr9XqtVms0qtXqHXVLVSqV61C5XL4KXf57e//47HS+vvv9n+FwPP71fX86PV24mLkJBUHwQj1TT9Qj5XneZBI+0HUcx7Zt0zQNw9B1/YF6pWJrWZpBuPRhPLVEIi2f3MmlaUpmgzBgfZ8jW3HChO1jkkgRJiRXyUrE/8ncUYycEEacYQpAmAIRpkCEKRBhCkSYAhGmQIQpEGEKRJgCEUMp55gCEKZAhCkQYQpEmAIRpkCEKRBhCkRMpbByt8/HWFpTsLJx2c0yszzKhXuwTDxVIJFWSO4dpLn5Si/SM73ZSu8PhT5giUJGXmAAAAAASUVORK5CYII=')] uppercase font-bold hidden  group-hover:inline-block
       z-10  bg-[#1f2d3d1c]
       absolute top-1/2 left-1/2 transform translate-x-[-50%] translate-y-[-50%] text-[#ebc86d] border 
       border-[#ebc86d] px-5 py-3
       w-[202px]
       ">Play for Game</button>
   </div>

 
</div>
</div>
  
</template>

<script>

export default {
  name: "SportCategory",
  components: {
    
  },
  data() {
    return {
      images: [
        require("../assets/images/category/card1.png"),
        require("../assets/images/category/card2.png"),
        require("../assets/images/category/card3.png"),
        require("../assets/images/category/card4.png"),
        
        
      ],
      active: 0,
    };
  },
};
</script>

<style scoped>
.container{
    max-width: 1200px;
}
</style>
