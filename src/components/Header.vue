
<template>
  <div class="font-sans antialiased" id="app">
    <nav class="flex items-center z-10 justify-between flex-wrap bg-white text-white p-6">
      <router-link to="/">
        <div class="flex items-center flex-no-shrink text-orange-500 mr-6">
          <svg
            class="fill-current h-8 w-8 mr-2"
            width="54"
            height="54"
            viewBox="0 0 54 54"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z"
            />
          </svg>
          <span class="font-semibold text-xl tracking-tight">Peexoo</span>
        </div>
      </router-link>
      <div class="block sm:hidden">
        <button
          @click="toggle"
          class="flex items-center px-3 py-2 border rounded text-orange-500 border-orange-500 hover:border-white"
        >
          <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <title>Menu</title>
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
          </svg>
        </button>
      </div>
      <div
        :class="open ? 'block': 'hidden'"
        class="w-full flex-grow sm:flex sm:items-center sm:w-auto"
      >
        <div class="text-sm sm:flex-grow"></div>
        <div>
          <router-link to="/about-us">
            <p class="m-2 p-2 md:inline text-left text-black opacity-50 text-sm">I am a Photographer</p>
          </router-link>
          <router-link to="/blog">
            <p class="m-2 p-2 md:inline text-left text-black opacity-50 text-sm">Explore Photos</p>
          </router-link>
          <router-link to="/products">
            <p class="m-2 p-2 md:inline text-left text-black opacity-50 text-sm">Find a Photographer</p>
          </router-link>
          <router-link to="/contact-us">
            <p class="m-2 p-2 md:inline text-left text-black opacity-50 text-sm">Find my Photos</p>
          </router-link>
          <router-link to="/contact-us">
            <p class="m-2 p-2 md:inline text-left text-orange-500 text-sm">Login or Register</p>
          </router-link>
        </div>
      </div>
    </nav>
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