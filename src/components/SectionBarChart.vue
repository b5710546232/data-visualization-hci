<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Category with the average rating</h1>
                    <h2 class="subtitle">
                        Bar chart represent the <strong>average</strong> rating of reviewer in each movie's category
                    </h2>
                    <div id="bar-chart"></div>
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
import csv_result from './csv/avg.csv'
import TopButton from './TopButton.vue'
console.log('csv',csv_result[0]);

export default {
    data () {
        return {}
    },
    computed: {},
    mounted () {            
        var chart = c3.generate({
            bindto: '#bar-chart',
    data: {
       x:'x',
        columns: [
            csv_result[0],
            csv_result[1]
            // ['category2', 3.480245, 3.503527, 3.576699, 3.353244, 3.394073, 3.632278, 3.632278, 3.687379, 3.215237, 3.921523, 3.290389, 3.521397, 3.638132, 3.621705, 3.560723 ]
        ],
        type: 'bar'
    },
    
    bar: {
        width: {
            ratio: 0.5 // this makes bar width 50% of length between ticks
        }
    },
    axis:{
        x:{type:'category',show:true},
         y: {
            label: 'rating'
        },
    },
})
    },
    methods: {},
    components: {
        TopButton
    }
}
</script>
<style scoped>
    #bar-chart {
        letter-spacing: 0px;
    }

</style>