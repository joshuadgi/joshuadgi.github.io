---
layout:
title: Just Calendar
permalink: /calendar/
---

<script type="text/javascript" src="/scripts/jquery-3.6.0.min.js"></script>
<script type="text/javascript" src="/scripts/moment.min.js"></script>
<script type="text/javascript" src="/scripts/fullcalendar.min.js"></script>
<script type="text/javascript" src="/scripts/rrule.min.js"></script>
<script type="text/javascript" src="/scripts/main.global.min.js"></script>
<link rel="stylesheet" href="//cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.2.0/fullcalendar.min.css">
<link rel="stylesheet" media="print" href="//cdnjs.cloudflare.com/ajax/libs/fullcalendar/3.2.0/fullcalendar.print.css">

<div id='calendar'></div>

<script>
var calendarEl = document.getElementById('calendar')
var calendar = new FullCalendar.Calendar(calendarEl, {
  initialView: 'dayGridMonth',
  validRange: {
    start: '2022-01-01'
  },
  events:[
  {
    title: 'Pagi 1',
    rrule: {
      dtstart: '2022-06-01',
      freq: 'daily',
      interval: 8
    }
  },
  {
    title: 'Pagi 2',
    rrule: {
      dtstart: '2022-06-02',
      freq: 'daily',
      interval: 8
    }
  },
  {
    title: 'Siang 1',
    rrule: {
      dtstart: '2022-06-03',
      freq: 'daily',
      interval: 8
    }
  },
  {
    title: 'Siang 2',
    rrule: {
      dtstart: '2022-06-04',
      freq: 'daily',
      interval: 8
    }
  },
  {
    title: 'Malam 1',
    rrule: {
      dtstart: '2022-06-05',
      freq: 'daily',
      interval: 8
    }
  },
  {
    title: 'Malam 2',
    rrule: {
      dtstart: '2022-06-06',
      freq: 'daily',
      interval: 8
    }
  }
  ]
})

calendar.render()
</script>
