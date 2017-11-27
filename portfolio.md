---
layout: default
---
# #portfolio

<!-- {% assign categories = "Experience, Projects, Personal" | split: ", " %}
{% for category in categories %}{% endfor %} -->
<section>
	{% assign items = site.portfolio | sort: "order" %}
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
