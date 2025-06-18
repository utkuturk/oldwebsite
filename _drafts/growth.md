---
title:  "Academic Growth"
layout: base
permalink: /growth/
---

# {{ page.title }}

This page shows the additional schools and seminars I have attended.

This demonstrates a two column timeline. TV Series use a timespan, but movies only have one date, so they demonstrate timeline events used without a `from` specified.

{% include jekyll-timeline.html
   startYear=2017
   timelineHeight=2500
   
   col1Title=""
   col1Events=site.data.growth
%}