---
title: "Events"
permalink: /events/

---
{page.event}
{page.calendar}
{page.calendar_id}

<div class="schedule">
	<h1 class="title">{{ page.title }}</h1>

	

	<section id="satur" class="day">
		<header>
			<h2>Saturday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>

		{% for post in site.categories.session reversed %}
			{% capture day %}{{ post.date | date: "%A" }}{% endcapture %}
			{% if day == 'Wednesday' %}
				{% include schedule-day.html %}
			{% endif %}
		{% endfor %}

	</section><!-- #satur.day -->

	<!-- section id="sun" class="day">
		<header>
			<h2>Sunday</h2>
			<span data-room="room-1">Room 1</span>
			<span data-room="room-2">Room 2</span>
			<span data-room="room-3">Room 3</span>
		</header>

		{% for post in site.categories.session reversed %}
		{% if post.day == 'Sunday' %}
			{% include schedule-day.html %}
		{% endif %}
		{% endfor %}

	</section><!-- #sun.day -->

</div><!-- .schedule -->
