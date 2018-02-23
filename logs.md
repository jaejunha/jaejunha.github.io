---
layout: default
---

# Logs  
<ul>
{% assign posts = site.TIL | sort: 'date' | reverse %}
{% for post in posts %}
        <li>
                <a href="{{ post.url }}">[{{ post.tag }}]{{ post.title }}
                <span style="float:right;"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d, %Y" }}</time></span>
                </a>
        </li>
{% endfor %}
</ul>

