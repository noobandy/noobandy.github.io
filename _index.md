---
layout: page
title: Anand Mohan
tagline: home
---
{% include JB/setup %}

## Blog Posts

{% for post in site.posts offset: 0 limit: 50 %}
<div class="row">
      <div class="span12">
		<h4><strong><a href="{{ post.url }}">{{ post.title }}</a></strong></h4>      
        <p>
          {{ post.summary }}
        </p>
		<p>
          <i class="glyphicon glyphicon-calendar"></i> {{ post.date | date: "%B %e, %Y" }}
          | <i class="glyphicon glyphicon-comment"></i> <a href="http://www.anandm.in{{ post.url }}#disqus_thread" data-disqus-identifier="{{ post.url }}"></a>     
		  | <i class="glyphicon glyphicon-tags"></i> Tags :{% for tag in post.tags %} <a href="/tags.html#{{ tag }}-ref" rel="tooltip" title="View posts tagged with &quot;{{ tag }}&quot;"><span class="label label-info">{{ tag }}</span></a>  {% if forloop.last != true %} {% endif %} {% endfor %}		            
        </p>
        <p><a href="{{ post.url }}">Read more</a></p>
      </div>
</div>
{% endfor %}



