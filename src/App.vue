<template>
  <div id="app">
    <Navbar id="my-navbar"></Navbar>
    <SectionIntro :title="'We have data since 1995-2015'" :subtitle="'of data\'s movie collection'"></SectionIntro>
    <SectionIntro :title="'There are 1,682 movies'" :subtitle="''"></SectionIntro>
    <SectionPie id="movie"></SectionPie>
    <SectionStackBarChart id="reviewer"></SectionStackBarChart> <!-- -->
    <!--<SectionSplineChart></SectionSplineChart>-->
    
    <SectionBarChart></SectionBarChart>
    <SectionMutiBarChart></SectionMutiBarChart>
    <SectionBubble id="trend"></SectionBubble>
    <SectionLineChart></SectionLineChart>
    <!--<SectionLineChart2></SectionLineChart2>-->
    <!--<SectionLineChart3></SectionLineChart3>-->
    <!--<SectionLineChart4></SectionLineChart4>-->
    <SectionConclusion></SectionConclusion>
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
import SectionMutiBarChart from './components/SectionMutiBarChart.vue'
import SectionLineChart from './components/SectionLineChart.vue'
import SectionLineChart2 from './components/SectionLineChart2.vue'
import SectionLineChart3 from './components/SectionLineChart3.vue'
import SectionLineChart4 from './components/SectionLineChart4.vue'
import SectionConclusion from './components/SectionConclusion.vue'
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
    SectionMember,
    SectionMutiBarChart,
    SectionLineChart,
    SectionLineChart2,
    SectionLineChart3,
    SectionLineChart4,
    SectionConclusion

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