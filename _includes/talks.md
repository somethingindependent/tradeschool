Trade School Talks are scheduled for Monday, July 23 &mdash; Thursday, July 26. Sessions will take place daily at 11am, 1pm and 3pm. 

All sessions take place live in the lobby of the Aloft Hotel located at 800 15th Street, on the corner of 15th and Stout St, in Downtown Denver.

{% assign talks_by_day = site.talks | where_exp: "item", "item.edition == site.current_edition" | sort: "date" | group_by_exp: "talk", "talk.date | date: '%A, %-m/%-d'" %}

{% if talks_by_day == empty %}
## SESSION SCHEDULE COMING SOON!
{% endif %}

{% for day in talks_by_day %}

## {{ day.items.first.date | date: '%A, %-m/%-d'" }}
{% for talk in day.items -%}
- [{{ talk.date | date: "%-I:%M %P" }} &mdash; {{ talk.title }}]({{ talk.url }})
{% endfor -%}
{%- endfor %}


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
