<template>
    <div class="root">
        <div>
            <section class="section  is-medium">
                <div class="container">
                    <div class="heading">
                        <h1 class="title">Popular of each movie category</h1>
                        <h2 class="subtitle">
                            showing the movie that have how many reviewer review on it.
                        </h2>
                        <div class="columns is-centered">
                            <svg id="bubble" width="600" height="580"></svg>
                        </div>
                        <h2 class="subtitle">
                            <strong>Drama</strong> has the most popular of all category. <strong>Documentory</strong> has the least popular of all category.
                        </h2>
                    </div>
                    <div class="columns is-pulled-right">
                       <TopButton></TopButton>
                    </div>
                </div>
            </section>
        </div>
    </div>
</template>
<script>
import * as d3 from "d3"
import TopButton from './TopButton.vue'
// import PATH_CSV from '../assets/flare.csv'
export default {
    data () {
        return {}
    },
    computed: {},
    mounted () {

var svg = d3.select("#bubble"),
    width = +svg.attr("width");

var format = d3.format(",d");

var color = d3.scaleOrdinal(d3.schemeCategory20c);

var pack = d3.pack()
    .size([width, width])
    .padding(1.5);

d3.csv('/src/assets/flare.csv', function(d) {
  d.value = +d.value;
  if (d.value) return d;
}, function(error, classes) {
  if (error) throw error;

  var root = d3.hierarchy({children: classes})
      .sum(function(d) { return d.value; })
      .each(function(d) {
        if (id = d.data.id) {
          var id, i = id.lastIndexOf(".");
          d.id = id;
          d.package = id.slice(0, i);
          d.class = id.slice(i + 1);
        }
      });

  var node = svg.selectAll(".node")
    .data(pack(root).leaves())
    .enter().append("g")
      .attr("class", "node")
      .attr("transform", function(d) { return "translate(" + d.x + "," + d.y + ")"; });

  node.append("circle")
      .attr("id", function(d) { return d.id; })
      .attr("r", function(d) { return d.r; })
      .style("fill", function(d) { return color(d.package); });

  node.append("clipPath")
      .attr("id", function(d) { return "clip-" + d.id; })
    .append("use")
      .attr("xlink:href", function(d) { return "#" + d.id; });

  node.append("text")
      .attr("clip-path", function(d) { return "url(#clip-" + d.id + ")"; })
    .selectAll("tspan")
    .data(function(d) { return d.class.split(/(?=[A-Z][^A-Z])/g); })
    .enter().append("tspan")
      .attr("x", 0)
      .attr("y", function(d, i, nodes) { return 13 + (i - nodes.length / 2 - 0.5) * 10; })
      .text(function(d) { return d; });

  node.append("title")
      .text(function(d) { return d.id + "\n" + format(d.value); });
})

    },
    methods: {},
    components: {TopButton}
}
</script>
<style scoped>
    text {
        /*font: 5px sans-serif;*/
        font-size: 1px;
        text-anchor: middle;
    }
</style>