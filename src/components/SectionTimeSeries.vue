<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Reviewer's Gender</h1>
                    <h2 class="subtitle">
                        The Chart show the number of each reviewer's gender from 943.
                    </h2>
                    <div id="time-series"></div>
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
    bindto: '#stack-bar',
    data: {
        x: 'x',
//        xFormat: '%Y%m%d', // 'xFormat' can be used as custom format of 'x'
        columns: [
            ['x', '2013-01-01', '2013-01-02', '2013-01-03', '2013-01-04', '2013-01-05', '2013-01-06'],
//            ['x', '20130101', '20130102', '20130103', '20130104', '20130105', '20130106'],
            ['data1', 30, 200, 100, 400, 150, 250],
            ['data2', 130, 340, 200, 500, 250, 350]
        ]
    },
    axis: {
        x: {
            type: 'timeseries'
            // tick: {
                // format: '%Y-%m-%d'
            // }
        }
    }
})
    },
    methods: {},
    components: {TopButton}
}
</script>
<style scoped>
    #stack-bar {
        letter-spacing: 0px;
    }
    .container.heading{
  margin-top: 10%;
}
</style>