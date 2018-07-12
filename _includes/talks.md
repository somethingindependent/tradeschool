<div class="centered-copy" markdown="1">
Trade School Talks are free & open to the public.

All sessions take place live in the lobby of the Aloft Hotel in Downtown Denver. \| [800 15th Street](https://maps.google.com/?q=800+15th+Street&entry=gmail&source=g), on the corner of 15th and Stout.

### Explore the schedule below. Click for discussion details and session speakers. Check back for session updates.

#### FEATURED SPEAKERS:

[Darcy Gaechter](http://adventuresportspodcast.libsyn.com/ep-381-first-woman-to-kayak-the-amazon-from-source-to-sea-darcy-gaechter), Adventurer/Kayaker \| [Luis Benitez](https://www.5280.com/2018/05/luis-benitez-talks-public-land-outdoor-retailer-utah-and-more/), Colorado Outdoor Rec \| [Tracy Ross](http://www.simonandschuster.com/authors/Tracy-Ross/67063419), Award-Winning Writer of the West \| [Shannon Galpin](https://endangeredactivism.org/the-team-1/), Endangered Activism \| [Madaleine Sorkin](https://www.climbing.com/news/madaleine-sorkin-and-the-aac-launch-the-climbing-grief-fund/), Climbing Grief Fund \| [Jason Blevins](https://twitter.com/jasonblevins?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor), Writer & Co-Founder, Colorado Sun \| [Tom Adams](https://business.utah.gov/outdoor/), Utah Outdoor Rec \|  [Mackenzie “Mack Daddy” McGrath](https://firstdescents.org/employees/mackenzie-mcgrath/), First Descents \| [Gretchen Jones](http://www.gretchenjones.co/), Award-Winning Fashion Director \| [Kelly Bastone](http://www.kellybastone.com/), Outdoor Journalist \| [Mely Whiting](https://www.tu.org/staff/Western%20Water%20and%20Habitat%20Program/melywhiting), Trout Unlimited \| [Cailin O’Brien-Feeney](https://www.snewsnet.com/people/cailin-obrien-feeney-leading-oregon-outdoor-recreation-office), Oregon Outdoor Rec Industry \| [Amy Kemp](https://twitter.com/skiergrrl?lang=en), Entrepreneur & All-Around Boss-Woman \| [Brendan Leonard](https://semi-rad.com/), Semi-Rad \|  [Kim Beekman](https://outdoorindustry.org/press-release/backbone-media-hires-former-skiing-magazine-editor-kim-beekman/), Backbone Media \| [Domenic Bravo](http://shifthistory.org/2017/speakers/domenic-bravo/), Wyoming Outdoor Rec \| [Rachel VandeVoort](https://flatheadbeacon.com/2017/10/04/rising-tide-outdoor-recreation/), Montana Outdoor Rec \| [Stacy Bare](https://wildideasworthliving.com/stacy-bare-using-adventure-to-help-veterans-yourself-and-others/), The Phoenix \|  [Scott McGuire](https://www.linkedin.com/in/mscottmcguire), Stoke Broker \| Female Founders & CEOs of [Bold Betties](https://www.boldbetties.com/), [Western Rise](https://westernrise.com/pages/company-philosophy),[Gearo](https://outdoorgearo.com/about-us/), [Wylder Goods](https://www.wyldergoods.com/pages/wylder-crew), [Heroclip](https://myheroclip.com/pages/about) \| [Camber Outdoors](https://camberoutdoors.org/) \| [American Whitewater](https://www.americanwhitewater.org/) \| [Backcountry Hunters & Anglers](http://www.backcountryhunters.org/) \| [Colorado Department of Natural Resources](https://cdnr.us/#/start) \| [American Alpine Club](https://americanalpineclub.org/) \| [Mayfly Outdoors](https://mayflyoutdoors.com/) \| [Grand Junction Economic Partnership and Riverfront at Las Colonias Park](https://riverfront.gjep.org/) \| [Colorado Outdoors Project](https://coloradooutdoors.co/) \| [Bonsai Design](http://www.bonsai-design.com/) \| [Access Fund](https://www.accessfund.org/)

</div>

{% assign talks_by_day = site.talks \| where_exp: "item", "item.edition == site.current_edition" \| sort: "date" \| group_by_exp: "talk", "talk.date \| date: '%A, %-m/%-d'" %}

{% if talks_by_day == empty %}
## SESSION SCHEDULE COMING SOON!
{% endif %}

{% for day in talks_by_day %}

## {{ day.items.first.date \| date: '%A, %-m/%-d'" }}
{% for talk in day.items -%}
- [{{ talk.date \| date: "%-I:%M %P" }} &mdash; {{ talk.title }}]({{ talk.url }})
{% endfor -%}
{%- endfor %}


### Use Google Calendar, iCal, or Outlook?
Subscribe to the full schedule and make it easy to look up all of the details on-the-go.
{% assign webcal_url = "schedule.ics" \| absolute_url \| replace: "http", "webcal" %}

<a class="calendar-button" href="{{ webcal_url }}">
  <i class="fa fa-calendar" aria-hidden="true"></i>
  Add to Outlook/iCal
</a>
<a class="calendar-button" href="http://www.google.com/calendar/render?cid={{ webcal_url }}" target="_blank">
  <i class="fa fa-calendar" aria-hidden="true"></i>
  Add to Google Calendar
</a>
