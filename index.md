---
layout: default 
---

# TIL   
---
## Englsh   
- [English](TIL/English/README)  
  
## Theory   
- [Graphics](TIL/Theory/Graphics/README)  
- [Network](TIL/Theory/Network/README)  
  
## Postech MCNL   
- [Seminar]()  
- [Daily]() 
 
---
# Post  
<ul>
{% for post in site.posts %}
	<li>
	<a href="{{ post.url }}">{{ post.title }}
	<span style="float:right;"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d, %Y" }}</time></span>
	</a>
	</li>
{% endfor %}
</ul>
