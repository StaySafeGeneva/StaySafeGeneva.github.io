---
layout: page
title: Luca's part
subtitle: a first test
---

Here are some trials, I hope you will enjoy them!
<hr>
<div class="chart"></div>
.chart div {
  font: 10px sans-serif;
  background-color: steelblue;
  text-align: right;
  padding: 3px;
  margin: 1px;
  color: white;
}
var data = [30, 86, 168, 281, 303, 365];

d3.select(".chart")
  .selectAll("div")
  .data(data)
    .enter()
    .append("div")
    .style("width", function(d) { return d + "px"; })
    .text(function(d) { return d; });



<hr>
<select id='race-10km' onchange="drawTimeWrtAge('10km');"></select>
<div id="timevsage-10km"></div>
