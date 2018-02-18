---
layout: default 
---

# TIL   
---
## Daily Study  
- [English](TIL/English/README)  
- [Graphics](TIL/Theory/Graphics/README)  
- [Network](TIL/Theory/Network/README)  
  
## Programming  
- [?]()  

---
# Log  
<ul>
{% assign posts = site.MCNL | sort: 'date' | reverse %}
{% for post in posts limit: 10 %}
        <li>
		<a href="{{ post.url }}">{{ post.tag }}
        	<span style="float:right;"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d, %Y" }}</time></span>
        	</a>
	</li>
{% endfor %}
</ul>
<h3><a style="color:#787878;float:right;" href="#">+more logs</a></h3>

