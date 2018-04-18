---
layout: default
---

# Logs  
<ul>
{% assign posts = site.TIL | sort: 'date' | reverse %}
{% assign counter = 0 %}
{% for post in posts %}
		{% assign counter = counter | plus:1 %}
        <li>
                <a href="{{ post.url }}">[{{ post.tag }}]{{ post.title }}
                <span style="float:right;"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d, %Y" }}</time></span>
                </a>
        </li>
{% endfor %}
</ul>

<script> 
	var tag_h1 = document.getElementsByTagName('h1').item(1); 
	var content = tag_h1.innerHTML;
	tag_h1.innerHTML = content+" ({{ counter }})";
</script>

