# Learning D3


<html>
<head>
  <meta charset="utf-8">
  <style type="text/css">
    svg {
      background-color: #b3e8c2;
      width: 400px;
      height: 400px;
    }
    circle {
      fill: #ff5200;
    }
  </style>
</head>
<body>
<svg></svg>
</body>
<script src="https://d3js.org/d3.v4.min.js"></script>
<script src="https://d3js.org/d3-timer.v1.min.js"></script>
<script type="text/javascript">
// Adapted from https://bl.ocks.org/pvernier/2ba5a32840c7d5125afe071c6b68e5ac
// Colors from sanzo R package.
  var circle = d3.select("svg")
                 .append("circle")
                 .attr("cx", 370)
                 .attr("cy", 200)
                 .attr("r", 30)
  d3.interval(function(elapsed) {
    circle.transition()
          .attr("cx", 200)
          .attr("cy", 370)
          .style("fill", "#FF616B")
          .transition()
          .attr("cx", 30)
          .attr("cy", 200)
          .style("fill", "C9303E")
          .transition()
          .attr("cx", 200)
          .attr("cy", 30)
          .style("fill", "681916")
          .transition()
          .attr("cx", 370)
          .attr("cy", 200)
          .style("fill", "C74300")
    }, 1000);
</script>
</html>
