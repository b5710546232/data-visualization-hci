<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Category with the gender's rating</h1>
                    <h2 class="subtitle">
                        Bar chart represent the rating of reviewer's' in each movie's category
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
            ['male\'s rating',4.860399666 ,4.559275141 ,4.899972119 ,3.204780806 ,2.786700891 ,4.436003442 ,2.615425622 ,4.061112361 ,2.183563282 ,2.090844457 ,1.422303479 ,2.726676553 ,1.279483786 ,2.830905749 ,2.423891508 ,3.328883786 ,3.206016433 ,1.073812315],
            ['female\'s rating', 2.134296409 ,1.14979166 ,1.298613135 ,1.235488494 ,2.765774838 ,2.474638137 ,4.763526423 ,3.451249202 ,1.171183901 ,2.919768906 ,1.244389708 ,4.073009368 ,1.672332989 ,1.347624996 ,3.622193734 ,4.525237316 ,2.518304044 ,4.527204557 ]
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