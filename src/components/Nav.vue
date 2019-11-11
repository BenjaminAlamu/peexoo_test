
<template>
  <div class="">
    <div class="bg-orange-500 p-4 flex flex-wrap justify-between">
      <img  />
      <div>
        <router-link to="/about-us">
          <p class="my-3 mx-12 font-bold p-2 md:inline text-left text-white text-base">Details</p>
        </router-link>
        <router-link to="/blog">
          <p class="my-3 mx-12 font-bold p-2 md:inline text-left text-white text-base">Portofolio</p>
        </router-link>
        <router-link to="/products">
          <p class="my-3 mx-12 font-bold p-2 md:inline text-left text-white text-base">Avaliablity</p>
        </router-link>
        <router-link to="/contact-us">
          <p class="my-3 mx-12 font-bold p-2 md:inline text-left text-white text-base">Pricing Packages</p>
        </router-link>
        <router-link to="/contact-us">
          <p class="my-3 mx-12 font-bold p-2 md:inline text-left text-white text-base">Reviews</p>
        </router-link>
      </div>
    </div>
    <div class="flex justify-between mt-4 mb-8 md:px-32">
      <p class="font-bold text-5xl">Afroshots</p>
      <div class="">
        <button class="border border-orange-500 p-2 m-2 text-orange-500 rounded-full font-bold p-2">Message Photographer</button>
        <button class="border bg-orange-500 p-2 m-2 text-white rounded-full font-bold p-2">Book Now</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      open: false
    };
  },
  methods: {
    toggle() {
      this.open = !this.open;
    }
  }
};
</script>

<style  scoped>
.myHeader {
  margin: 0 !important;
}
.logo {
  height: 40px;
  width: 40px;
  margin: 2px;
}
</style>