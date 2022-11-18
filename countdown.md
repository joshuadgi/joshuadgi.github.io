---
layout: default
title: Just Countdown
permalink: /countdown/
---


<script type="text/javascript" src="/scripts/jquery-1.11.3.min.js"></script>
<script type="text/javascript" src="/scripts/jquery.plugin.min.js"></script>
<script type="text/javascript" src="/scripts/jquery.countdown.min.js"></script>
<link rel="stylesheet" href="/assets/css/jquery.countdown.css">
<link rel="stylesheet" href="/assets/css/style.css">

<h1 class="background-highlight">{{site.name}}</h1>
<a href="{{site.externalLink}}"><img src="/assets/img/countdown.png" /></a>

<div id="defaultCountdown"></div>

<h2 class="background-highlight">{{ site.utc | date: "%A %B %-d, %Y" }}</h2>

<script type="text/javascript">
  	$(function () {
        var dday = new Date();
        dday = new Date("{{site.utc}}");
        $('#defaultCountdown').countdown({until: dday});
        $('#year').text(dday.getFullYear());
    });
</script>