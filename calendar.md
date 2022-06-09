---
layout: page
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
<link href='https://cdn.jsdelivr.net/npm/bootstrap@4.5.0/dist/css/bootstrap.css' rel='stylesheet'>
<link href='https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.13.1/css/all.css' rel='stylesheet'>

<div id='calendar'></div>

<script>
document.addEventListener('DOMContentLoaded', function(){
  var calendarEl = document.getElementById('calendar');
  var calendar = new FullCalendar.Calendar(calendarEl, {
    themeSystem: 'bootstrap',
    height: '100%',
    customButtons: {
      prevMo: {
        text: 'Prev Month',
        click: function(){
          calendar.prev();
        }
      },
      nextMo: {
        text: 'Next Month',
        click: function(){
          calendar.next();
        }
      },
      goToday: {
        text: 'Today',
        click: function(){
          calendar.today();
        }
      }
    },
    headerToolbar: {
      start: '',
      center: 'title',
      end: ''
    },
    footerToolbar: {
      start: 'goToday',
      center: '',
      end: 'prevMo,nextMo'
    },
    initialView: 'dayGridMonth',
    events:[
    {
      start: $('#calendar').fullCalendar('today'),
      display: 'background',
      color: '#51f06c'
      },
    {
      title: 'Pagi 1',
      display: 'background',
      color: '#4287f5',
      rrule: {
        dtstart: '2022-06-01',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Pagi 2',
      display: 'background',
      color: '#4287f5',
      rrule: {
        dtstart: '2022-06-02',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Siang 1',
      display: 'background',
      color: '#fff587',
      rrule: {
        dtstart: '2022-06-03',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Siang 2',
      display: 'background',
      color: '#fff587',
      rrule: {
        dtstart: '2022-06-04',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Malam 1',
      display: 'background',
      color: '#8339fa',
      rrule: {
        dtstart: '2022-06-05',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Malam 2',
      display: 'background',
      color: '#8339fa',
      rrule: {
        dtstart: '2022-06-06',
        freq: 'daily',
        interval: 8
      }
    }
    ]
  });
  calendar.render();
  });
</script>
