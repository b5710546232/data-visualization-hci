<template>
    <div class="wrapper">
        <nav class="nav nav-upper">
            <div class="nav-center is-active">
                <div class="nav-item title">Movie Data Visualization</div>
            </div>
        </nav>
        <nav class="nav has-shadow">
            <div class="nav-center is-active">
                <div class="nav-item sub-menu "><a href="">Graph1</a></div>
                <div class="nav-item sub-menu "><a href="">Graph1</a></div>
                <div class="nav-item sub-menu "><a href="">Graph1</a></div>
            </div>
        </nav>
</template>
<script>
export default {
  data(){
    return {}
  },
  methods:{

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