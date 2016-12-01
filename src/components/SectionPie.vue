<template>
    <div>
        <section class="section  is-large">
         <div class="container">
      <div class="heading">
        <h1 class="title">Section</h1>
        <h2 class="subtitle">
          A simple container to divide your page into <strong>sections</strong>, like the one you're currently reading
        </h2>
        <div id="pie"></div>
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
            bindto: '#pie',
            data: {
                // iris data from R
                columns: [
                    ['data1', 30],
                    ['data2', 120],
                ],
            type : 'pie',
            onclick: function (d, i) { console.log("onclick", d, i); },
            onmouseover: function (d, i) { console.log("onmouseover", d, i); },
            onmouseout: function (d, i) { console.log("onmouseout", d, i); }
    }
})
    },
    methods: {},
    components: {}
}
</script>
<style scoped>

</style>