---
layout: page
title: Running
permalink: /running/
---


![Me]({{site.url}}/img/running.png){:style="width: 400px;float: left;margin-right: 14px;margin-top: 7px;"}
<br><br><br>
###  <span style="color:blue"> Prochaine course : <a href="https://www.trailcotedopale.com/"> Trail Côte d'Opale </a> (31 km) </span>
<br><br><br><br><br><br><br>

<br>


<section class="post-list">
	<div class="container">
		{% for post in site.categories.Running%}
			{% unless post.next %}
				<h2 class="category-title">{{ post.date | date: '%Y' }}</h2>
			{% else %}
				{% capture year %}{{ post.date | date: '%Y' }}{% endcapture %}
				{% capture nyear %}{{ post.next.date | date: '%Y' }}{% endcapture %}
				{% if year != nyear %}
					<h2 class="category-title">{{ post.date | date: '%Y' }}</h2>
				{% endif %}
			{% endunless %}
			<article class="post-item">
			<span class="post-meta date-label">{{ post.date | date: "%b %d" }}</span>
			<div class="article-title"><a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></div>
			</article>
		{% endfor %}
	</div>

</section>

##### En 2017
Vainqueur Trail Sainte Victoire  
2eme Trail des Cabornis (20km)  
​20 km de Lausanne, 12eme en 1h06'05 

##### En 2016
10 km foulées Sanpriotes, 4eme en 32’04   
Semi Annecy 3eme Français en 1h10’40  
Vainqueur Nocturne des Teppes - 2016  
7eme au Triathlon du Semnoz LD  
​