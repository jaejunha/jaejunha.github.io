---
layout: default 
---

# TIL   
---
## Language  
- (PAUSE)[English](/tag?value=English)  

## Theory  
- (PAUSE)[Graphics](/tag?value=Graphics)  
- (PAUSE)[Network](/tag?value=Network)  
  
## Programming  
- [HTML5](/tag?value=HTML5)    
- [CSS](/tag?value=CSS)    
- [jQuery](/tag?value=jQuery)  
- [Android](/tag?value=Android)  
- [Jekyll](/tag?value=Jekyll)  
- [Django](/tag?value=Django)  
- [Markdown](/tag?value=Markdown)  
- [Git](/tag?value=Git)  

## OS  
- [Ubuntu](/tag?value=Ubuntu)  
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

