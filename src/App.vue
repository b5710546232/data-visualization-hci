<template>
  <div id="app">
    <Navbar></Navbar>
    <SectionIntro :title="'22 year data...'" :subtitle="'of data\'s movie collection'"></SectionIntro>
    <SectionIntro :title="'A lot of movies'" :subtitle="'1,682 movies'"></SectionIntro>
    <SectionPie></SectionPie>
  </div>
</template>

<script>
import SectionIntro from './components/SectionIntro.vue'
import SectionPie from './components/SectionPie.vue'
import Navbar from './components/Navbar.vue'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    SectionPie,
    Navbar,
    SectionIntro
  }
}
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /*text-align: center;*/
    color: #2c3e50;
    /*margin-top: 60px;*/
  }
  
  h1,
  h2 {
    font-weight: normal;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    display: inline-block;
    margin: 0 10px;
  }
  
  a {
    color: #42b983;
  }
</style>