---
layout: default 
---

# TIL   
---
## Language  
- [English](/tag?value=English)  

## Theory  
- [Graphics](/tag?value=Graphics)  
- [Network](/tag?value=Network)  
  
## Programming  
- [Android](/tag?value=Android)  
- [CSS](/tag?value=CSS)    
- [jQuery](/tag?value=jQuery)  
- [Jekyll](/tag?value=Jekyll)  
- [Markdown](/tag?value=Markdown)  
- [Git](/tag?value=Git)  

## OS  
- [Kali](/tag?value=Kali)  

---
# Recent  
<ul>
{% assign posts = site.TIL | sort: 'date' | reverse %}
{% for post in posts limit: 5 %}
        <li>
    	<a href="{{ post.url }}">[{{ post.tag }}]{{ post.title }}
        	<span style="float:right;"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d, %Y" }}</time></span>
        	</a>
    </li>
{% endfor %}
</ul>
<h3><a style="color:#787878;float:right;" href="logs">+more logs</a></h3>

