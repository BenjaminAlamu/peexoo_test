<template>
  <div id="app">
    <Header/>
    <Landing/>
    <Nav/>
    <div  class="flex mt-12 mb-8">
      <SingleCalendar class="w-1/2 mx-auto"/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Nav from './components/Nav.vue'
import Landing from './components/Landing.vue'
import SingleCalendar from './components/SingleCalendar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    Header,
    SingleCalendar,
    Landing,
    Nav,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Montserrat', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
