<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Reviewer's Gender</h1>
                    <h2 class="subtitle">
                        The Chart show the number of each reviewer's gender from <strong>943</strong> reviewer.
                    </h2>
                    <div id="stack-bar"></div>
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
        columns: [
            ['male', 670],
            ['female', 273 ],
        ],
        type: 'bar',
        groups: [
            ['male', 'female']
        ]
    },
    grid: {
        y: {
            lines: [{value:0}]
        }
    },
        axis: {
        rotated: true
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