---
layout: default
title: Thank you for contacting us
permalink: /thanks/
contact: false
---

<div id="container" class="home">
  <div class="content">
    <div class="marquee">
      {% for post in site.categories.careers %}
      {% capture openings %}{{ post.active }}{% endcapture %}
      {% if post.active == "true" %}
      <a href="{{ site.baseurl }}/careers" id="hiring">We Hiring!</a>
      {% endif %}
      {% endfor %}
      <div class="site-width">
        <div class="background"></div>
        <div class="leadin">
         <h1>Thanks for getting in touch.</h1>
         <h2>We'll get back to you shortly. In the meantime, please continue to explore.</h2>
       </div>
     </div>
   </div>
 </div>
</div>
<div class="home-nav">
  <ul class="large-block-grid-3 navblocks">
    <li>
      <div class="content">
        <a href="{{ site.baseurl }}/team"><h3>We are forward-thinking technologists with heart.</h3><span class="rubric">Meet our team</span></a>
      </div>
    </li>
    <li>
      <div class="content">
        <a href="{{ site.baseurl }}/expertise"><h3>We provide compelling strategy and web solutions.</h3><span class="rubric">Learn about our services</span></a>
      </div>
    </li>
    <li>
      <div class="content">
        <a href="{{ site.baseurl }}/work"><h3>We proudly partner with mission-driven organizations.</h3><span class="rubric">Explore our work</span></a>
      </div>
    </li>
  </ul>
</div>
<div class="main">
  <ul id="most-recent-blog" class="large-block-grid-3">
    {% for post in site.categories.blog limit:3 %}
    <li>
      <div class="quote">
        <h3 class="post-title"><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title}}</a></h3>
        <p>{{ post.date | date: "%B %-d, %Y" }}</p>
      </div>
    </li>
    {% endfor %}
	</ul>
</div>