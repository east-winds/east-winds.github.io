---
layout: page
subtitle: Michael Davidson
use-site-title: true
published: true
---

<br>

**I currently have two openings for Postdoctoral Researchers:**

- [Political Economy of Power Grid Management](/2020-05-30-postdoc-political-economy-power-grid-management/)
- [Flexible Thermo-Electric Systems](/2020-06-08-postdoc-flexible-thermoelectric-systems/)


I am an assistant professor in the [School of Global Policy and Strategy](http://gps.ucsd.edu/) and the [Mechanical and Aerospace Engineering Department](http://maeweb.ucsd.edu/) at the University of California, San Diego. My research and teaching center on the **engineering implications** and **institutional conflicts** inherent in deploying **low-carbon energy at scale**. I have a particular interest in understanding the **political systems of Asia** (with a focus on China and India), as well as the **western U.S.**

My [research topics](/research/) include renewable resource assessments, power system operations, and political economy of markets:

[![Research topics](/img/index_images.png)](/research/)

<br>

I welcome inquiries by prospective PhD applicants and postdoctoral fellows, as well as UC San Diego students interested in conducting research. Consult my list of  [academic programs and mentoring opportunities](/mentoring/).

I am a faculty member with the [21st Century China Center][21ccc] and the [Center for Commerce and Diplomacy][ccd], both located at UC San Diego. I am also an associate in the [Environment and Natural Resources Program][enrp] at the Harvard Kennedy School Belfer Center, and a fellow with the [Initiative for Sustainable Energy Policy](http://sais-isep.org/), hosted at Johns Hopkins SAIS. Read more [here](/aboutme/).

<br>
<br>

<div class="posts-list">
  {% if site.tags["home"] %}
  <div style="text-align:center"><i><h4>News</h4></i></div>
  {% endif %}
  {% for post in site.tags["home"] %}
  <article class="post-preview">
    <a href="{{ post.url | prepend: site.baseurl }}">
	  <h3 class="post-title">{{ post.title }}</h3>

	  {% if post.subtitle %}
	  <h4 class="post-subtitle">
	    {{ post.subtitle }}
	  </h4>
	  {% endif %}
    </a>

    <p class="post-meta">
      {{ post.date | date: "%B %-d, %Y" }}
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
        {% if post.content != post.excerpt %}
          <a href="{{ post.url | prepend: site.baseurl }}" class="post-read-more">[Read&nbsp;More]</a>
        {% endif %}
      </div>
    </div>

	{% comment %}
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
	{% endcomment %}

   </article>
  {% endfor %}
</div>



{% comment %}
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
{% endcomment %}


[21ccc]: http://china.ucsd.edu/
[ccd]: http://ccd.ucsd.edu/
[belfer]: https://www.belfercenter.org/
[enrp]: https://www.belfercenter.org/program/environment-and-natural-resources
