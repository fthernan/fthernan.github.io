---
layout: default
---
# #portfolio

{% assign categories = "Experience, Projects" | split: ", " %}
{% for category in categories %}
<section>
	<h3>{{ category }}</h3>
	{% assign items = site.portfolio | where: "category", category | sort: "order" %}
	{% for item in items %}
	<div class="portfolio_item thumb_size_{{ item.thumbsize }}">
	  <a href="{{ item.url | prepend: site.baseurl }}">
	    <img src="{{ site.baseurl }}/images/{{ item.title | downcase }}/thumb.jpg" />
	    <div class="title">{{ item.title }}</div>
	  </a>
	  <div class="tags">{{ item.tags |  join: ", " }}</div>
	</div>
	{% endfor %}
</section>
{% endfor %}
