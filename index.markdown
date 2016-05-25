---

---
<head>
	<link rel="stylesheet" type="text/css" href="/css/main.css">
</head>>
<body>

<div id="header">
Seeds Gallery
</div>

<div id="nav">
{% for category in site.categories %}
  <li><a name="{{ category | first }}">{{ category | first }}</a>
    <ul>
    {% for posts in category %}
      {% for post in posts %}
      	{% if post.url %}
	        <li><a href="{{ post.url }}">{{ post.name }}</a></li>
	  	{% endif %}    
      {% endfor %}
    {% endfor %}
    </ul>
  </li>
{% endfor %}
</div>

<div id="section">
    {% for post in site.posts %}
       	{% if post.url %}
	        <div id="boxes">
	        	<div id="article">
	        		<table>
	        		<tr>
	        			<th>
		        		{{ post.name }}
		        		</th>
		        	</tr>
		        	<tr>
		        		<td>
		        			<a href="{{ post.url }}">
		        				<img src="photos_small/{{ post.seed-image }}" />
		        			</a>
		        		</td>
		        	</tr>
		        	</table>
	        	</div>
	        </div>
	  	{% endif %}    
    {% endfor %}
</div>

<div id="footer">
Copyright © W3Schools.com
</div>

</body>
