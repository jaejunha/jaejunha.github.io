---
layout: default 
---

# Recent  
---
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
<br>

# TIL   
---

## Theory  
- [Graphics](/tag?value=Graphics)  
- [MultiMedia](/tag?value=MultiMedia)  
- [Network](/tag?value=Network)  
- [AI](/tag?value=AI)  

## Programming  
- [HTML5](/tag?value=HTML5)    
- [CSS](/tag?value=CSS)    
- [jQuery](/tag?value=jQuery)  
- [Three.js](/tag?value=Three.js)  
- [Android](/tag?value=Android)  
- [Jekyll](/tag?value=Jekyll)  
- [Django](/tag?value=Django)  
- [Markdown](/tag?value=Markdown)  
  
## Tool  
- [Git](/tag?value=Git)  
- [Wings3D](/tag?value=Wings3D)  
- [Blender](/tag?value=Blender)  
  
## OS  
- [Ubuntu](/tag?value=Ubuntu)  

<script>
        var tags = {}
        {% assign posts =  site.TIL %}
        {% assign before = "" %}
        {% for post in posts %}
        if(tags["{{post.tag}}"])
                tags["{{post.tag}}"]++;
        else
                tags["{{post.tag}}"]=1;
        {% endfor %}

        var tag_a = document.getElementsByTagName('a');
        var name;
        for(var i=0;i<tag_a.length;i++){
                if((name = tag_a.item(i).innerHTML).indexOf('<') == -1){
                		if(tags[name])
    						tag_a.item(i).innerHTML = name+" ("+tags[name]+")";
                }
        }
</script>
