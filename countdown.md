---
layout: page
title: Just Countdown
permalink: /countdown/
---



<!-- Font from google -->
<link href='//fonts.googleapis.com/css?family=Open+Sans:400,700,800' rel='stylesheet' type='text/css'>
<!-- bootstrap -->
<link href="/assets/css/bootstrap.min.css" rel="stylesheet">
<!-- countdown css -->
<link rel="stylesheet" href="/assets/css/jquery.countdown.css">
<!-- custom styles -->
<link rel="stylesheet" href="/assets/css/style.css">

<div class="row">
      <div class="col-sm-12 text-center">
			<h1 class="background-highlight">{{site.name}}</h1>
	       <a href="{{site.externalLink}}"><img src="/assets/img/countdown.png" style="width:100%"/></a>
      </div>
    </div> <!-- /row -->

<div class="row">
    <div class="col-sm-8 col-sm-offset-2 text-center"><div id="defaultCountdown"></div></div>
</div> <!-- /row -->

<div class="row">
    <div class="col-sm-12 text-center">
        <h2 class="background-highlight">{{ site.utc | date: "%A %B %-d, %Y" }}</h2>
    </div>
</div>

<!-- javascript includes
    ================================================== -->
<!-- Placed at the end of the document so the pages load faster -->

<!-- jquery  -->
<script type="text/javascript" src="/assets/js/jquery-1.11.3.js"></script>

<!-- countdown code -->
<script src="/assets/js/jquery.countdown.js"></script>

<!-- start the countdown when the page loads -->
<script type="text/javascript">
  	$(function () {
  		var holiday = new Date();
  		holiday = new Date("{{site.utc}}");
  		$('#defaultCountdown').countdown({until: holiday});
  		$('#year').text(holiday.getFullYear());
  	});
</script>
<!-- end of javascript includes  -->