---
layout: default
---

<div id="div_list"></div>
<script>
var string_tag = window.location.search.split('=')[1];
var string_html = "<h1>"+string_tag+"</h1><ul>";
{% assign posts = site.TIL | sort: 'date' | reverse %}
{% for post in posts %}
        if(string_tag == "{{post.tag}}"){
	string_html+="<li>";	
                string_html+='<a href="{{ post.url }}">[{{ post.tag }}]{{ post.title }}';
                string_html+='<span style="float:right;"><time datetime="{{ post.date | date:"%d-%m-%Y" }}">{{ post.date | date: "%b %d, %Y" }}</time></span>';
                string_html+='</a>';
        string_html+='</li>';
	}
{% endfor %}
string_html+="</ul>"
document.getElementById('div_list').innerHTML=string_html;
</script>

