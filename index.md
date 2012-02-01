---
layout: default
title: Home
group: navigation
---
{% include JB/setup %}

### Blog Posts: 

<div class="related">
<div class="accordion" id="accordian2">
  {% for post in site.posts %}
	<div class="accordion-group">
		<div class="accordion-heading">
			<div class="rightdate">{{ post.date | date: "%B %e, %Y" }}</div>
			<a class="accordion-toggle" data-toggle="collapse" data-parent="#accordian2" data-target="#section-{{ post.uniqueid }}"> 
				{{ post.title }}
			</a>
		</div>
		<div id="section-{{ post.uniqueid }}" class="accordion-body collapse">
			<div class="accordion-inner">
				{{ post.content }}
				<a href="{{ post.url }}">Permanent Link to Post</a>
			</div>
		</div>
	</div>
  {% endfor %}
</div>
</div>