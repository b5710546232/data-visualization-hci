<template>
    <div>
        <section class="section  is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Movie Category</h1>
                    <h2 class="subtitle">
                        Pie chart show the movie of <strong>18</strong> category in percentage.
                    </h2>
                    <div id="pie"></div>
                    <h2 class="subtitle">
                            From 1682 movie, we can categorize in to 18 category. <strong>Drama</strong> has the most movie in all category.
                    </h2>
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
import c3 from 'c3'
import TopButton from './TopButton.vue'
export default {
    data () {
        return {}
    },
    computed: {},
    mounted () {
        const chart = c3.generate({
            bindto: '#pie',
            data: {
                // iris data from R
                columns: [
                ['Action',25589],
                ['Adventure',13753],
                ['Animation',3605],
                ['Children.s',7182],
                ['Comedy',29832],
                ['Crime',8055],
                ['Documentary',758],
                ['Drama',39895],
                ['Fantasy',1352],
                ['Film-Noir',1733],
                ['Horror',5317],
                ['Musical',4954],
                ['Mystery',5245],
                ['Romance',19461],
                ['Sci-Fi',12730],
                ['Thriller',21872],
                ['War',9398],
                ['Western',1854]
                ],
            type : 'pie',
            onclick:  (d, i)=> { console.log("onclick", d, i); },
            onmouseover:  (d, i)=> { console.log("onmouseover", d, i); },
            onmouseout:  (d, i) => { console.log("onmouseout", d, i); }
    }
})
    },
    methods: {},
    components: {TopButton}
}
</script>
<style scoped>
    #pie {
        letter-spacing: 0px;
    }
</style>