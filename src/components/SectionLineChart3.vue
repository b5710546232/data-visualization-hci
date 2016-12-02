<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Category with the average rating</h1>
                    <h2 class="subtitle">
                        Bar chart represent the <strong>average</strong> rating of reviewer in each movie's category
                    </h2>
                    <div id="line-chart-3"></div>
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
            bindto: '#line-chart-3',
    data: {
       x:'x',
        columns: [
            ['x','1995', '1996', '1997', '1998', '1999', '2000', '2001', '2002', '2003', '2004', '2005', '2006', '2007', '2008', '2009', '2010', '2011', '2012', '2013', '2014', '2015'],
            // ['Action' ,2,3,5,3,2,3,5,5,5,3,5,2,1,3,5,2,1,3,5,2,5],
            // ['Adventure' ,5,4,3,1,1,4,5,5,5,5,3,5,4,5,1,5,2,5,2,2,2],
            // ['Animation' ,4,1,4,2,4,5,5,1,1,3,4,3,1,2,2,5,3,5,4,2,3],
            // ['Children.s' ,1,4,1,3,2,2,2,5,5,2,3,3,5,2,1,1,5,5,4,4,1],
            // ['Comedy' ,1,1,4,4,1,3,2,1,1,1,5,2,4,4,2,4,1,2,5,3,1]
            // ['Crime' ,2,5,4,4,1,4,4,2,5,3,2,2,2,5,5,3,4,2,2,3,3],
            // ['Documentary' ,1,5,5,4,3,2,5,4,1,2,4,3,1,1,1,5,2,4,4,5,5],
            // ['Drama' ,1,3,4,5,3,4,4,4,4,1,1,5,2,5,1,5,5,2,2,3,1],
            // ['Fantasy' ,4,3,3,2,4,5,4,4,1,4,1,1,5,4,1,1,4,5,1,3,3],
            // ['Film.Noir' ,5,5,2,5,4,4,2,4,3,3,2,5,3,2,5,4,4,4,4,3,2],
            // ['Horror' ,3,5,4,5,3,2,2,1,4,2,1,2,4,4,5,2,4,4,1,5,1]
            ['Musical' ,1,5,4,4,1,3,5,3,3,5,3,4,4,1,4,2,5,1,2,2,4],
            ['Mystery' ,1,2,4,1,4,1,3,4,1,2,3,4,2,4,5,5,3,5,5,2,2],
            ['Romance' ,5,3,5,2,1,2,4,2,1,2,4,3,2,1,4,3,5,1,2,1,4],
            ['Sci.Fi' ,1,5,1,2,3,3,5,3,5,1,2,1,3,1,4,2,3,2,4,5,1],
            // ['Thriller' ,3,3,3,3,3,3,1,1,1,3,4,1,4,2,5,4,2,3,3,4,1],
            // ['War' ,1,2,3,1,5,4,4,1,5,5,3,5,2,4,2,5,4,3,5,3,4],
            // ['Western' ,3,4,1,3,3,3,3,3,4,5,4,3,4,1,4,2,5,4,1,5,4]

            // ['category2', 3.480245, 3.503527, 3.576699, 3.353244, 3.394073, 3.632278, 3.632278, 3.687379, 3.215237, 3.921523, 3.290389, 3.521397, 3.638132, 3.621705, 3.560723 ]
        ],
        type: 'line'
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
    #line-chart-3 {
        letter-spacing: -1px;
    }

</style>