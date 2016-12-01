<template>
 <div>
        <section class="section  is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Reference of data</h1>
                    <h2 class="subtitle">We get the data from <strong>Movielent</strong> </h2>
                    <h3 class="subtitle">Non-commercial, personalized movie recommendations.</h3>
                </div>
                <div class="content">
                <a href="https://movielens.org">Link to Movielent</a>
                </div>
                <div class="columns is-pulled-right">
                   <TopButton></TopButton>
                </div>
                <!--<div id="pie"></div>-->
            </div>
        </section>
    </div>
</template>
<script>
export default {
    data () {
        return {}
    },
    computed: {},
    mounted () {},
    methods: {},
    components: {}
}
</script>
<style scoped>
.title{
    font-size: 52px;
}
.content{
    padding-top: 5%;
    font-size: 32px;
}
</style>