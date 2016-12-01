<template>
    <div class="wrapper">
        <nav class="nav nav-upper">
            <div class="nav-center is-active">
                <div class="nav-item title">Movie Data Visualization</div>
            </div>
        </nav>
        <nav class="nav has-shadow">
            <div class="nav-center is-active">
                <a class="nav-item sub-menu" href="#" @click="scollTo('#movie')" >Movie</a>
                <a class="nav-item sub-menu" href="#" @click="scollTo('#reviewer')" >Reviewer</a>
                <a class="nav-item sub-menu" href="#" @click="scollTo('#trend')" >Trend</a>
                <a class="nav-item sub-menu" href="#" @click="scollTo('#reference')" >Reference</a>
                <a class="nav-item sub-menu" href="#" @click="scollTo('#member')" >Member</a>
            </div>
        </nav>
</template>
<script>
import scrollToElement from 'scroll-to-element'
export default {
  data(){
    return {}
  },
  methods:{
 scollTo(e){
      event.preventDefault()
      scrollToElement(e, {
        offset: 0,
        ease: 'outBack',
        duration: 500
      })
    },
  },
  components:{}
  
}
</script>
<style scoped>
    .wrapper {
        top: 0;
        /*position: relative;
        top: 0;
        left: 0;
        width: 100%;
        height: 50px;
        z-index: 9999;
        margin: 0px auto;*/
    }
    
    .nav {
        background: rgb(34, 208, 178);
    }
    
    .title {
        font-size: 42px;
        color: white;
    }
    
    .sub-menu {
        font-size: 32px;
        color: white;
    }
    
    a {
        color: white;
    }
    
    a:hover {
        color: black;
    }
</style>