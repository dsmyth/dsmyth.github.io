---
layout: post
title: Learning Python with a little GeoJSON
---

Trying to teach myself a little Python, decided to tinker a bit with GeoJSON.

Whipped up a quick script that read data from the Seattle City Health Inspector results 
database & spurts out a GeoJSON file that show inspected restaurants with the latest inspection results.

Those with a "satisfactory" result are coded green. Those with an "unsatisfactory" result are coded red. Otherwise, they are grey.

<script src="https://embed.github.com/view/geojson/dsmyth/seattlehealthgeojson/master/inspections.geojson?height=540&width=800"></script>

Here's the (very simple) code if you are interested: [Seattle 98105 Health Inspection Results](https://github.com/dsmyth/seattlehealthgeojson)
