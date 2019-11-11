<template>
  <div id="app">
    <Header />
    <Landing />
    <Nav />
    <div class="bg-orange-100">
      <div class="flex flex-wrap mx-auto justify-center md:justify-between md:px-32 pt-4">
        <p class="font-bold text-5xl">
          Afroshots
          <i class="fas fa-clipboard-check"></i>
        </p>
        <div class>
          <button
            class="border border-orange-500 p-2 m-2 text-orange-500 rounded-full font-bold p-2"
          >Message Photographer</button>
          <button
            class="border bg-orange-500 p-2 m-2 text-white rounded-full font-bold p-2"
          >Book Now</button>
        </div>
      </div>
      <div class="flex pt-4">
        <SingleCalendar class="w-full md:w-1/2 mx-auto" />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Nav from "./components/Nav.vue";
import Landing from "./components/Landing.vue";
import SingleCalendar from "./components/SingleCalendar.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    SingleCalendar,
    Landing,
    Nav,
    Footer
  }
};
</script>

<style>
#app {
  font-family: "Montserrat", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
