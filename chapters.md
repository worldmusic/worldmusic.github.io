---
layout: default
title: "Chapters"
description: "An ever-expanding table of contents"
---
Words about the chapters... Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<center>
  <a href="{{ site.baseurl }}/call/" class="btn">Contribute a chapter</a>
  <a href="{{ site.baseurl }}/about/" class="btn">More about the project</a>
</center>

## Filter by Tag

<div id = "tagList"></div>

## Chapters

<div id = "itemList">
    {% assign chapters = site.pages | where: "layout", "chapter" | sort:'date' | reverse %}
    {% for chapter in chapters %}
      <div class = "item">
        {% include chapter.html chapter=chapter %}
      </div>
    {% endfor %}
</div>

<div class="top-border">
<p>
<center>
  <a href="{{ site.baseurl }}/resources" class="btn">Other resources</a>
</center>
</p>
</div>

{% include tag-script.html %}
