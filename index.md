---
layout: default 
---

# Recent  
---
<ul>
{% assign posts = site.TIL | sort: 'date' | reverse %}
{% for post in posts limit: 5 %}
        <li>
    	<a href="{{ post.url }}">
		{{ post.title }}<br>
		<span>[{{ post.tag }}]</span>
        	<time datetime="{{ post.date | date:"%d-%m-%Y" }}" style="float:right;">{{ post.date | date: "%b %d, %Y" }}</time>
        	</a>
	</li>
{% endfor %}
</ul>
<h3><a style="color:#787878;float:right;" href="logs">+more logs</a></h3>
<br>
# TIL   
---

<div class="div_tag" markdown="1">

## Theory  
- [Graphics](javascript:void(0))  
- [MultiMedia](javascript:void(0))  
- [Network](javascript:void(0))  

## Test  
- [Opic](javascript:void(0))  

## Algorithm  
- [Key](javascript:void(0))  
- [Library](javascript:void(0))  
- [Advance](javascript:void(0))  
- [PS](javascript:void(0))  

## Programming  
- [HTML5](javascript:void(0))    
- [CSS](javascript:void(0))    
- [jQuery](javascript:void(0))  
- [Node.js](javascript:void(0))  
- [Three.js](javascript:void(0))  
- [Java](javascript:void(0))  
- [Android](javascript:void(0))  
- [Python](javascript:void(0))  
- [Django](javascript:void(0))  
- [Jekyll](javascript:void(0))  
- [Markdown](javascript:void(0))  
  
## Tool  
- [Git](javascript:void(0))  
- [Wings3D](javascript:void(0))  
- [Blender](javascript:void(0))  
- [Illustrator](javascript:void(0))  
- [PhotoShop](javascript:void(0))  
  
## OS  
- [Ubuntu](javascript:void(0))  

</div>
<div class="div_tag"></div>
<script>
	$('.div_tag').css('float','left');
        $('.div_tag:nth-of-type(1)').css('width',$('section').width()*0.4);
        $('.div_tag:nth-of-type(2)').css('width',$('section').width()*0.6);

	showTag("{{ posts.first.tag }}");
	
	    var tags = {}
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
	            		if(tags[name]){
						tag_a.item(i).innerHTML = name+" ("+tags[name]+")";
					tag_a.item(i).setAttribute('href','javascript:showTag("'+name+'")');
				}
	            }
	    }
	
	function showTag(name){
		var string_tag = name;
	    	var string_html = "<h2>&gt&nbsp;"+string_tag+"</h2><ul>";
	   	 	{% for post in posts %}
	    	if(string_tag == "{{post.tag}}"){
	            	string_html+='<li><a href="{{ post.url }}">{{ post.title }}';
	            	string_html+='</a></li>';
	    	}
	    	{% endfor %}
		string_html+="</ul>";
	    
	    	$('.div_tag:nth-of-type(2)').html(string_html);
	}
</script>
