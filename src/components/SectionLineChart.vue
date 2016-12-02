<template>
    <div>
        <section class="section is-mobile is-medium">
            <div class="container">
                <div class="heading">
                    <h1 class="title">Category with number of reviewers</h1>
                    <h2 class="subtitle">
                        Line chart represent category of number reviewerers in each years.
                    </h2>
                    <div id="line-chart"></div>
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
import result from './csv/line.csv'
import TopButton from './TopButton.vue'
export default {
    data () {
        return {}
    },
    computed: {},
    mounted () {
        var chart = c3.generate({
            bindto: '#line-chart',
    data: {
       x:'x',
        columns: [
            result[0],result[1],result[2],result[3],result[4]
            // ['x','1995', '1996', '1997', '1998', '1999', '2000', '2001', '2002', '2003', '2004', '2005', '2006', '2007', '2008', '2009', '2010', '2011', '2012', '2013', '2014', '2015'],
            // ['Action' ,72, 75, 22, 20, 93, 76, 60, 47, 90, 88, 56, 49, 41, 55, 72, 14, 8, 35, 3, 69, 12],
            // ['Adventure' ,1, 56, 55, 28, 75, 96, 88, 75, 3, 45, 30, 72, 83, 11, 24, 46, 46, 68, 8, 70, 9],
            // ['Animation' ,71, 45, 96, 77, 31, 59, 53, 95, 22, 58, 30, 41, 73, 55, 50, 85, 36, 9, 7, 32, 42],
            // ['Children.s' ,70, 64, 42, 20, 47, 68, 97, 93, 19, 26, 30, 71, 35, 14, 55, 49, 93, 37, 65, 84, 70],
            // ['Comedy' ,41, 47, 52, 57, 26, 46, 53, 55, 23, 41, 93, 61, 77, 51, 6, 96, 37, 91, 52, 5, 69],
            // ['Crime' ,75, 61, 74, 23, 3, 38, 33, 48, 67, 36, 2, 72, 25, 10, 32, 17, 56, 11, 37, 80, 79],
            // ['Documentary' ,47, 93, 80, 18, 11, 46, 20, 29, 96, 4, 32, 66, 87, 84, 82, 73, 69, 41, 22, 37, 76],
            // ['Drama', 78, 65, 51, 54, 87, 95, 26, 29, 48, 29, 47, 8, 15, 70, 61, 73, 10, 94, 92, 74, 26],
            // ['Fantasy' ,55, 32, 24, 62, 59, 94, 72, 43, 34, 48, 92, 32, 5, 80, 84, 31, 59, 42, 44, 39, 30],
            // ['Film.Noir' ,22, 11, 78, 25, 66, 98, 98, 46, 29, 29, 27, 65, 30, 10, 19, 39, 23, 78, 8, 76, 69],
            // ['Horror' ,15, 100, 38, 3, 90, 28, 60, 91, 42, 91, 89, 90, 47, 1, 65, 53, 91, 73, 19, 87, 15],
            // ['Musical' ,84, 76, 4, 49, 32, 14, 76, 76, 44, 79, 72, 30, 36, 35, 61, 13, 79, 54, 58, 15, 68],
            // ['Mystery' ,56, 42, 22, 88, 93, 51, 66, 77, 30, 93, 54, 48, 28, 25, 86, 2, 2, 44, 87, 3, 1],
            // ['Romance' ,38, 99, 54, 10, 47, 62, 95, 12, 36, 24, 70, 69, 83, 43, 54, 64, 14, 89, 52, 57, 83]
            // ['Sci.Fi' ,90, 11, 31, 57, 43, 18, 24, 32, 100, 45, 12, 18, 56, 33, 6, 79, 70, 88, 5, 70, 86],
            // ['Thriller' ,14, 73, 96, 50, 89, 97, 6, 29, 99, 61, 49, 24, 26, 49, 34, 67, 58, 15, 85, 39, 86],
            // ['War' ,51, 86, 90, 46, 49, 7, 43, 87, 62, 31, 97, 58, 46, 71, 39, 16, 39, 2, 31, 72, 20],
            // ['Western' ,93, 53, 59, 43, 1, 55, 54, 67, 22, 67, 30, 46, 25, 3, 48, 74, 39, 16, 83, 17, 79],

            // ['category2', 3.480245, 3.503527, 3.576699, 3.353244, 3.394073, 3.632278, 3.632278, 3.687379, 3.215237, 3.921523, 3.290389, 3.521397, 3.638132, 3.621705, 3.560723 ]
        ],
        type: 'spline'
    },
    
    bar: {
        width: {
            ratio: 0.5 // this makes bar width 50% of length between ticks
        }
    },
    axis:{
        x:{type:'category',show:true},
          y: {
            label: 'People'
        },
    },
});
    },
    methods: {},
    components: {
        TopButton
    }
}
</script>
<style scoped>
    #line-chart {
        letter-spacing: 0px;
    }

</style>