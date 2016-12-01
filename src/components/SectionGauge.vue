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
                    <div id="gauge"></div>
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
                <!--<div id="pie"></div>-->
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
            bindto: '#gauge',
        data: {
        columns: [
            ['data1', 30],
            ['data2', 70]
        ],
        type: 'gauge',
        onclick: function (d, i) { console.log("onclick", d, i); },
        onmouseover: function (d, i) { console.log("onmouseover", d, i); },
        onmouseout: function (d, i) { console.log("onmouseout", d, i); }
    },
    color: {
        pattern: ['#FF0000', '#F97600', '#F6C600', '#60B044'], // the three color levels for the percentage values.
        threshold: {
//            unit: 'value', // percentage is default
//            max: 200, // 100 is default
            values: [30, 60, 90, 100]
        }
    },
    size: {
        height: 180
    }
})
    },
    methods: {},
    components: {}
}
</script>
<style scoped>
    #gauge {
        letter-spacing: 0px;
    }
</style>