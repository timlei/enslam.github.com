---
layout: default
title: Tags
permalink: /
---
<div class="tabbable tabs-left" id="tags">
	<ul class="nav tabs nav-tabs">
	{% for tag in site.tags %}
		<li><a href="#{{ tag[0] }}" title="{{ tag[0] }}" rel="{{ tag[1].size }}" data-toggle="tab">{{ tag[0] }}</a></li>
	{% endfor %}
	</ul>
	<div class="tab-content">
	{% for tag in site.tags %}
		<div class="tab-pane" id="{{ tag[0] }}">
			<ul>
				{% for post in tag[1] %}
					<li>
						<a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
					</li>
				{% endfor %}
			</ul>
		</div>
	{% endfor %}
	</div>
</div>