Five days of inspirational and educational talks that get you thinking about the nature of real work. 

<span class="disclaimer">
Please be aware that Understudy is an intimate venue with limited seating available for sessions. We can accommodate about 40 people. If you’re planning to attend a session, please arrive early knowing that even arriving early does not guarantee access. Each session will also be streamed live on Facebook, and aired simultaneously at [The Commons on Champa](http://thecommons.co/).
</span>

### Use Google Calendar, iCal, or Outlook?
Subscribe to the full schedule and make it easy to look up all of the details on-the-go.
{% assign webcal_url = "schedule.ics" | absolute_url | replace: "http", "webcal" %}

<a class="calendar-button" href="{{ webcal_url }}">
  <i class="fa fa-calendar" aria-hidden="true"></i>
  Add to Outlook/iCal
</a>
<a class="calendar-button" href="http://www.google.com/calendar/render?cid={{ webcal_url }}" target="_blank">
  <i class="fa fa-calendar" aria-hidden="true"></i>
  Add to Google Calendar
</a>

{% assign talks_by_day = site.talks | sort: "date" | group_by_exp: "talk", "talk.date | date: '%A, %-m/%-d'" %}

{% for day in talks_by_day %}

## {{ day.items.first.date | date: '%A, %-m/%-d'" }}
{% for talk in day.items -%}
- [{{ talk.date | date: "%-I:%M %P" }} &mdash; {{ talk.title }}]({{ talk.url }})
{% endfor -%}
{%- endfor -%}
