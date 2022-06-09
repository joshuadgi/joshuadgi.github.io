---
layout: page
title: Just Calendar
permalink: /calendar/
---

<script type="text/javascript" src="/scripts/jquery-3.6.0.min.js"></script>
<script type="text/javascript" src="/scripts/moment.min.js"></script>
<script type="text/javascript" src="/assets/fullcalendar/main.min.js"></script>
<script type="text/javascript" src="/scripts/rrule.min.js"></script>
<script type="text/javascript" src="/scripts/main.global.min.js"></script>
<link rel="stylesheet" href="/assets/fullcalendar/main.min.css">

<div id='calendar'></div>

<script>
document.addEventListener('DOMContentLoaded', function(){
  var calendarEl = document.getElementById('calendar');
  var calendar = new FullCalendar.Calendar(calendarEl, {
    initialView: 'dayGridMonth',
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
    events:[
    {
      title: 'Today',
      start: 'today',
      display: 'background',
      color: '#b50000',
      allDay: 'true'
      },
    {
      title: 'Pagi 1',
      textColor: '#ffffff',
      display: 'background',
      color: '#089e80',
      allDay: 'true',
      rrule: {
        dtstart: '2022-06-01',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Pagi 2',
      textColor: '#ffffff',
      display: 'background',
      color: '#089e80',
      allDay: 'true',
      rrule: {
        dtstart: '2022-06-02',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Siang 1',
      textColor: '#ffffff',
      display: 'background',
      color: '#bf6a15',
      allDay: 'true',
      rrule: {
        dtstart: '2022-06-03',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Siang 2',
      textColor: '#ffffff',
      display: 'background',
      color: '#bf6a15',
      allDay: 'true',
      rrule: {
        dtstart: '2022-06-04',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Malam 1',
      textColor: '#ffffff',
      display: 'background',
      color: '#132c3b',
      allDay: 'true',
      rrule: {
        dtstart: '2022-06-05',
        freq: 'daily',
        interval: 8
      }
    },
    {
      title: 'Malam 2',
      textColor: '#ffffff',
      display: 'background',
      color: '#132c3b',
      allDay: 'true',
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
