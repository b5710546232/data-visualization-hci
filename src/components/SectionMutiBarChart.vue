<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Category with the average rating</h1>
                    <h2 class="subtitle">
                        Bar chart represent the <strong>average</strong> rating of reviewer in each movie's category
                    </h2>
                    <div id="bar-mutichart"></div>
                </div>
                <div class="columns is-pulled-right">
                   <TopButton></TopButton>
                </div>
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
        var chart = c3.generate({
            bindto: '#bar-mutichart',
    data: {
       x:'x',
        columns: [
            ['x', 'Action', 'Adventure', 'Animation', 'Children\'s', 'Comedy', 'Crime', 'Documentary', 'Drama', 'Fantasy', 'Film-Noir', 'Horror', 'Musical', 'Mystery', 'Romance', 'Sci-Fi ' ],
            ['male',2.920927442 ,4.275773486 ,1.679906539 ,3.837567704 ,1.078777656 ,1.604448166 ,1.704852842 ,1.979531099 ,2.096718504 ,3.815091357 ,0.278452074 ,2.368185644 ,4.220674838 ,2.733471757 ,0.049480587 ,4.093480579 ,3.154727023 ,2.000734903],
            ['female',0.818759896 ,0.811598335 ,2.942484596 ,2.925595112 ,1.875717533 ,1.062512603 ,0.126388299 ,4.122669215 ,0.759184578 ,1.456663319 ,4.005725188 ,3.104783839 ,0.870624599 ,3.763688881 ,3.118947302 ,3.274510066 ,2.970337899 ,3.539560186]
        ],
        type: 'bar'
    },
    
    bar: {
        width: {
            ratio: 0.5 // this makes bar width 50% of length between ticks
        }
    },
    axis:{x:{type:'category',show:true}},
});
    },
    methods: {},
    components: {
        TopButton
    }
}
</script>
<style scoped>
    #bar-mutichart {
        letter-spacing: 0px;
    }

</style>