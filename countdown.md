---
layout: default
title: Just Countdown
permalink: /countdown/
---


<script type="text/javascript" src="/scripts/jquery-1.11.3.min.js"></script>
<script type="text/javascript" src="/scripts/jquery.plugin.min.js"></script>
<script type="text/javascript" src="/scripts/jquery.countdown.min.js"></script>
<link rel="stylesheet" href="/assets/css/jquery.countdown.css">
<link href='//fonts.googleapis.com/css?family=Open+Sans:400,700,800' rel='stylesheet' type='text/css'>>
<link href="assets/css/bootstrap.min.css" rel="stylesheet">


<div class="row">
    <div class="col-sm-12 text-center">
		<h1 class="background-highlight">{{site.name}}</h1>
	    <a href="{{site.externalLink}}"><img src="/assets/img/countdown.png"/></a>
    </div>
</div> 

<div class="row">
    <div class="col-sm-8 col-sm-offset-2 text-center"><div id="defaultCountdown"></div></div>
</div>

<div class="row">
    <div class="col-sm-12 text-center">
        <h2 class="background-highlight">{{ site.utc | date: "%A %B %-d, %Y" }}</h2>
    </div>
</div>

<script>
    var dday = new Date();
    dday = new Date("{{site.utc}}");
    $('#defaultCountdown').countdown({until: dday});
    $('#year').text(dday.getFullYear());
</script>