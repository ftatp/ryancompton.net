---
layout: page
title: Blog
tagline:
---
{% include JB/setup %}

  <ul class="posts">
    {% for post in site.posts %}
      <li>
        <span class="post-date">{{ post.date | date: "%b %-d, %Y" }}</span>
        <a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        {% if post.excerpt_tag %}
          {{ post.excerpt_tag | markdownify }}
        {% else %}
          {{ post.content }}
        {% endif %}
        <a href="{{ post.url | prepend: site.baseurl }}">Read more...</a>
      </li>
      <hr>
    {% endfor %}
  </ul>

  <footer>
      <div class="container">
        <p>&copy; {{ site.time | date: '%Y' }} {{ site.author.name }}
          with help from <a href="http://jekyllbootstrap.com" target="_blank" title="The Definitive Jekyll Blogging Framework">Jekyll Bootstrap</a>
          and <a href="http://github.com/dhulihan/hooligan" target="_blank">The Hooligan Theme</a>
        </p>
      </div>
 </footer>


