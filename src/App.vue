<template>
  <div id="app">
    <Navbar id="my-navbar"></Navbar>
    <SectionIntro :title="'22 year data...'" :subtitle="'of data\'s movie collection'"></SectionIntro>
    <SectionIntro :title="'A lot of movies'" :subtitle="'1,682 movies'"></SectionIntro>
    <SectionPie id="movie"></SectionPie>
    <SectionStackBarChart id="reviewer"></SectionStackBarChart> <!-- -->
    <!--<SectionSplineChart></SectionSplineChart>-->
    <SectionBubble id="trend"></SectionBubble>
    <SectionBarChart></SectionBarChart>
    <SectionReference id="reference"></SectionReference>
    <SectionMember id="member"></SectionMember>
  </div>
</template>

<script>
import SectionIntro from './components/SectionIntro.vue'
import SectionSplineChart from './components/SectionSplineChart.vue'
import SectionPie from './components/SectionPie.vue'
import SectionBarChart from './components/SectionBarChart.vue'
import SectionStackBarChart from './components/SectionStackBarChart.vue'
import SectionBubble from './components/SectionBubble.vue'
import Navbar from './components/Navbar.vue'
import SectionReference from './components/SectionReference.vue'
import SectionMember from './components/SectionMember.vue'
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
    SectionBarChart,
    SectionBubble,
    SectionSplineChart,
    SectionStackBarChart,
    SectionIntro,
    SectionReference,
    SectionMember
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
  
  /*h1,
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
  }*/
</style>