<template>
    <div>
        <section class="section  is-large">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Section</h1>
                    <h2 class="subtitle">
                        A simple container to divide your page into <strong>sections</strong>, like the one you're currently
                        reading
                    </h2>
                    <div id="spline"></div>
                </div>
                <div class="columns is-pulled-right">
                    <a href="#my-navbar">
                        <span>
                                <span class="columns">
                                    <i class="fa fa-arrow-up fa-5x"></i>
                                </span>
                        <span class="columns is-centered">
                                    Go to top
                                </span>
                        </span>
                    </a>
                </div>
            </div>
        </section>
    </div>
</template>
<script>
import c3 from 'c3'
export default {
    data () {
        return {}
    },
    computed: {},
    mounted () {
        const chart = c3.generate({
            bindto: '#spline',
            data: {
                columns: [
                    ['male', 24, 24, 23, 42, 57, 36, 29,53,47,45,21,30,40,26,25,39,49,32,41,7,38,33,28,22,37,16,27,50,31,17,19,20],
                    ['data2', 130, 100, 140, 200, 150, 50]
                ],
                type: 'spline'
            }
        })
    },
    methods: {},
    components: {}
}
</script>
<style scoped>
    #spline {
        letter-spacing: 0px;
    }
</style>