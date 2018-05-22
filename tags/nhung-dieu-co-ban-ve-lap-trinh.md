---
layout: default
title: Những điều cơ bản về lập trình
excerpt: Những kiến thức cơ bản nhất về ngành lập trình viên, công nghệ thông tin, chia sẻ cách để học lập trình một cách nhanh và hiệu quả nhất, những kinh nghiệm quý báu dành cho người mới học. Những đam mê và khó khăn trên con đường trở thành lập trình viên
permalink: /tags/nhung-dieu-co-ban-ve-lap-trinh
---
<div id="index">
<div class="category_detail">
    <h1>{{page.title}}</h1>
    <p>{{page.excerpt}}</p>
</div>
{% for post in site.posts %}
{% if post.tags contains 'nhung-dieu-co-ban-ve-lap-trinh' %}
<article class="post" itemscope itemtype="http://schema.org/Article">
  <h1 itemprop="name"><a itemprop="url" href="{{ site.site_url }}{{ post.url }}" title="{{ post.title | xml_escape }}" >{{ post.title | xml_escape }}</a></h1>
  {% if post.thumbnail %}
  <a href="{{ post.url }}"><img itemprop="image" src="{{ site.site_url }}/images/{{ post.thumbnail }}" alt="{{ post.title | xml_escape }}" class="post_thumbnail"></a>
  {% else %}
  <a href="{{ post.url }}"><img itemprop="image" src="{{ site.site_url }}/images/thumbnail_default.png" alt="{{ post.title  | xml_escape }}" class="post_thumbnail"></a>
  {% endif %}
  <div class="excerpt" itemprop="description">
    {{ post.excerpt }}
  </div>
  <div class="clear"></div>
</article>
{%endif%}
{% endfor %}
</div>