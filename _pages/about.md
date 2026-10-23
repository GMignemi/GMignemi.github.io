---
permalink: /
title: "Profile"
author_profile: true
redirect_from: 
- /about/
- /about.html
---
I am Assistant Professor of Psychometrics and Measurement Models at the *Department of Social Sciences* of *[Kore University](https://uke.it/en)*.

I was previously research fellow at the *[Institute of Computer Science](https://www.cs.cas.cz/comps/team.html)* of the *Czech Academy of Science*, under the supervision of [Patricia Martinkova](https://www.cs.cas.cz/martinkova/) and postdoctoral fellow at the *Bocconi Institute for Data Science and Analytics [BIDSA](https://bidsa.unibocconi.eu/people/faculty)* under the joint supervision of [Antonio Lijoi](https://didattica.unibocconi.it/mypage/index.php?IdUte=189615&amp%3Bcognome=LIJOI&amp%3Bnome=ANTONIO&amp%3BurlBackMy=) and [Igor Pruenster](https://mypage.unibocconi.eu/igorpruenster/).  

I earned my PhD in Psychometrics in 2024 from the *Department of General Psychology* at the *University of Padova* under the supervision of [Andrea Spoto](https://dpg.unipd.it/category/ruoli/personale-docente?key=6DB5058FD70BCB294F3B6A43724D4A02) and [Antonio Calcagni](https://antonio-calcagni.eu/). I spent the last year of my PhD visiting the *Statistics Departments* of *UCL* and *LSE* collaborating with [Ioanna Manolopoulou](https://ioannamanolopoulou.github.io/), [Yunxiao Chen](https://www.lse.ac.uk/statistics/people/yunxiao-chen) and [Irini Moustaki](https://irmoustaki.github.io/).

You can find a [CV here.](http://GMignemi.github.io/files/CV_Giuseppe_Mignemi_26.pdf)


Research interests
======
My main research interests are:

- Discrete Latent Structure in Educational Data
- Bayesian Hierarchical Models
- Bayesian Nonparametrics
- Latent Variable Models 
- Inter-Rater Reliability Analysis

News!
======
- New preprint on arXiv, joint work with Daniele Tancini and Francesco Bartolucci: *Generalized Infinite Hidden Markov Models* [arXiv:2610.31337](https://arxiv.org/abs/2610.31337v1).

- I am delighted to have been awarded an **MSCA Fellowships CZ** grant! I will be joining the [COMputational PSychometrics group](https://www.cs.cas.cz/comps/index.html) at the *Institute of Computer Science* of the *Czech Academy of Sciences*. See more [awards and grants](https://www.cs.cas.cz/comps/funding.html).

- New preprint on arXiv, joint work with Sally Paganin and Patricia Martinkova: [arXiv:2610.14199](https://doi.org/10.48550/arXiv.2610.14199).

- I am pleased to have been awarded [Marie Skłodowska-Curie Actions - Seal of Excellence](https://marie-sklodowska-curie-actions.ec.europa.eu/) for the project: 
BABEL - BAyesian Biclustering models for hEterogeneous Learning.


Collaboration network
======
<div id="collab-map" style="width:100%; max-width:900px; margin: 1.5em 0;"></div>
<div id="collab-legend" style="display:flex; flex-wrap:wrap; gap:8px 20px; margin-top:0.8em; font-size:13px;"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/7.8.5/d3.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/topojson/3.0.2/topojson.min.js"></script>
<script>
(function () {
  var points = [
    { n: 1,  city: "Padova, Italy",              inst: "Home base",                          lat: 45.40, lon:  11.90, hub: true },
    { n: 2,  city: "Milan, Italy",                inst: "Bocconi University",                 lat: 45.46, lon:   9.19 },
    { n: 3,  city: "Perugia, Italy",               inst: "University of Perugia",              lat: 43.11, lon:  12.39 },
    { n: 4,  city: "London, UK",                   inst: "LSE / UCL",                          lat: 51.50, lon:  -0.12 },
    { n: 5,  city: "Prague, Czech Republic",       inst: "Czech Academy of Sciences",          lat: 50.08, lon:  14.44 },
    { n: 6,  city: "Columbus, Ohio, USA",          inst: "Ohio State University",              lat: 39.96, lon: -83.00 },
    { n: 7,  city: "Enna, Sicily",                 inst: "Kore University",                    lat: 37.57, lon:  14.28 },
    { n: 8,  city: "Urbana-Champaign, USA",        inst: "University of Illinois",             lat: 40.11, lon: -88.20 },
    { n: 9,  city: "Seattle, USA",                 inst: "University of Washington",           lat: 47.61, lon: -122.33 },
    { n: 10, city: "Coleraine, Northern Ireland",  inst: "Ulster University",                  lat: 55.13, lon:  -6.67 },
    { n: 11, city: "Sheffield, UK",                inst: "University of Sheffield",             lat: 53.38, lon:  -1.47 },
    { n: 12, city: "Manchester, UK",               inst: "University of Manchester",            lat: 53.48, lon:  -2.24 },
    { n: 13, city: "Egham, UK",                    inst: "Royal Holloway, University of London",lat: 51.43, lon:  -0.56 },
    { n: 14, city: "Liverpool, UK",                inst: "University of Liverpool",             lat: 53.41, lon:  -2.98 },
    { n: 15, city: "Maynooth, Ireland",            inst: "Maynooth University",                lat: 53.38, lon:  -6.59 },
    { n: 16, city: "Dublin, Ireland",              inst: "Trinity College Dublin",              lat: 53.34, lon:  -6.26 },
    { n: 17, city: "Madrid, Spain",                inst: "Complutense University of Madrid",    lat: 40.42, lon:  -3.70 }
  ];

  var hub = points.filter(function (p) { return p.hub; })[0];
  var others = points.filter(function (p) { return !p.hub; });

  var landColor  = "#e3e1d8";
  var strokeColor = "#ffffff";
  var hubColor   = "#D85A30";
  var nodeColor  = "#1D9E75";
  var lineColor  = "#D85A30";

  var svg = d3.select("#collab-map").append("svg")
    .attr("viewBox", "0 0 680 400")
    .attr("width", "100%")
    .attr("height", "auto");

  var projection = d3.geoNaturalEarth1().scale(115).translate([230, 190]).rotate([40, 0]);
  var path = d3.geoPath(projection);

  d3.json("https://cdn.jsdelivr.net/npm/world-atlas@2/countries-110m.json").then(function (world) {
    var countries = topojson.feature(world, world.objects.countries).features;

    svg.selectAll("path.country").data(countries).join("path")
      .attr("class", "country").attr("d", path)
      .attr("fill", landColor).attr("stroke", strokeColor).attr("stroke-width", 0.5);

    var hubXY = projection([hub.lon, hub.lat]);
    others.forEach(function (p) {
      var xy = projection([p.lon, p.lat]);
      var mx = (hubXY[0] + xy[0]) / 2, my = Math.min(hubXY[1], xy[1]) - 35;
      svg.append("path")
        .attr("d", "M" + hubXY[0] + "," + hubXY[1] + " Q" + mx + "," + my + " " + xy[0] + "," + xy[1])
        .attr("fill", "none").attr("stroke", lineColor).attr("stroke-width", 0.8).attr("opacity", 0.45);
    });

    points.forEach(function (p) {
      var xy = projection([p.lon, p.lat]);
      var g = svg.append("g");
      g.append("title").text(p.city + " — " + p.inst);
      g.append("circle").attr("cx", xy[0]).attr("cy", xy[1]).attr("r", p.hub ? 8 : 5)
        .attr("fill", p.hub ? hubColor : nodeColor).attr("stroke", strokeColor).attr("stroke-width", 0.8);
      g.append("text").attr("x", xy[0]).attr("y", xy[1]).attr("text-anchor", "middle")
        .attr("dominant-baseline", "central").attr("font-size", p.hub ? "9px" : "7px")
        .attr("font-weight", "600").attr("fill", "#fff").text(p.n);
    });
  });

  var legend = d3.select("#collab-legend");
  points.forEach(function (p) {
    var row = legend.append("div").style("display", "flex").style("align-items", "center").style("gap", "6px");
    row.append("span").style("width", "16px").style("height", "16px").style("border-radius", "50%")
      .style("background", p.hub ? hubColor : nodeColor).style("color", "#fff").style("font-size", "9px")
      .style("font-weight", "600").style("display", "flex").style("align-items", "center")
      .style("justify-content", "center").style("flex", "0 0 auto").text(p.n);
    row.append("span").text(p.city + " — " + p.inst);
  });
})();
</script>
