---
layout: page
title: Stay Safe Geneva!
subtitle: An analysis of the accidents in Geneva
use-site-title: true
---
# Front page

![](../img/Geneva panorama.jpg)

It still has to be written!

### Ideas
- What about as logo a half swiss cross and half health cross?
- Maps? We should decide soon!
$\frac{1}{2}$

### To the team:
- In the **pages** folder you will find a markdown file with your name. Feel free to experiment in it and if you feel so begin to write your part. Note that you can also write it in jupyter notebook and then copy and paste it whenever you feel like it!.  
**NOTE:** If you write it in jupyter notebook, it will be about the same, but try out sometimes that the sintax is the same than here: e.g. if you want to include latex (like it is easily done in jupyter notebook) we should include a piece of code for it, so keep me updated! :)
- Feel free to modify the _about.md_ in **pages** folder as well, it is written by the team, for the team ;)
- If you wish you can also modify this file (i.e. _index.md_ in the global directory) but please be careful!
- For the other files, if you are not sure of what you are doing, do not hesitate to contact me :) you can also experiment on your local copy of the website!  

### Special thanks:

- Leaflet [examples](http://leafletjs.com/examples.html)
- [Bokeh plots and jekyll](https://briancaffey.github.io/2017/01/23/bokeh-plots-on-jekyll.html)  
- Bokeh doc used intensivly, espescially about [components](http://bokeh.pydata.org/en/latest/docs/user_guide/embed.html#components)  
- The [Texas interactive plot](https://bokeh.pydata.org/en/latest/docs/gallery/texas.html) from bokeh
- Some [Basis](https://www.w3schools.com/html/html_css.asp) for understanding HTML, CSS and JS
- For [bar plots](https://scrimba.com/p/pEKMsN/cast-1953) (even if not used yet)
- [Video](https://www.youtube.com/watch?v=SWVjQsvQocA) about Jekyll


[//]:#(---------- END OF WHAT IS VISIBLE ----------------)

[//]:#(The rest here is useless for the moment, it is the code for the posts :p
  i.e. if we wanna be able to make posts on our website we should put back index.html :) )

<div class="posts-list">
  {% for post in paginator.posts %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	  <h2 class="post-title">{{ post.title }}</h2>

	  {% if post.subtitle %}
	  <h3 class="post-subtitle">
	    {{ post.subtitle }}
	  </h3>
	  {% endif %}
    </a>

    <p class="post-meta">
      Posted on {{ post.date | date: "%B %-d, %Y" }}
    </p>

    <div class="post-entry-container">
      {% if post.image %}
      <div class="post-image">
        <a href="{{ post.url | prepend: site.baseurl }}">
          <img src="{{ post.image }}">
        </a>
      </div>
      {% endif %}
      <div class="post-entry">
        {{ post.excerpt | strip_html | xml_escape | truncatewords: site.excerpt_length }}
        {% assign excerpt_word_count = post.excerpt | number_of_words %}
        {% if post.content != post.excerpt or excerpt_word_count > site.excerpt_length %}
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
        {% endif %}
      </div>
    </div>

    {% if post.tags.size > 0 %}
    <div class="blog-tags">
      Tags:
      {% if site.link-tags %}
      {% for tag in post.tags %}
      <a href="{{ site.baseurl }}/tag/{{ tag }}">{{ tag }}</a>
      {% endfor %}
      {% else %}
        {{ post.tags | join: ", " }}
      {% endif %}
    </div>
    {% endif %}

   </article>
  {% endfor %}
</div>

{% if paginator.total_pages > 1 %}
<ul class="pager main-pager">
  {% if paginator.previous_page %}
  <li class="previous">
    <a href="{{ paginator.previous_page_path | prepend: site.baseurl | replace: '//', '/' }}">&larr; Newer Posts</a>
  </li>
  {% endif %}
  {% if paginator.next_page %}
  <li class="next">
    <a href="{{ paginator.next_page_path | prepend: site.baseurl | replace: '//', '/' }}">Older Posts &rarr;</a>
  </li>
  {% endif %}
</ul>
{% endif %}
