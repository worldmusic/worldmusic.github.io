---
layout: default
title: "Chapters"
description: "An ever-expanding table of contents"
---
## About WMT Chapters

The World Music Textbook is comprised of "chapters." These are prepared by scholars, musicians, and others and they go through a blind peer review process. They may be short essays, videos, interactive sites, or they may be in other formats entirely. If you have an idea for a contribution, please reach out or consider submitting. In addition to these chapters, the [resources]({{ site.baseurl }}/resources/) page lists many other useful sites from across the internet.

<p>
<center>
  <a href="{{ site.baseurl }}/call/" class="btn">Contribute a chapter</a>
  <a href="{{ site.baseurl }}/resources" class="btn">Other resources</a>
  <a href="{{ site.baseurl }}/about/" class="btn">More about the project</a>
</center>
</p>

## Chapters

<div id = "tagList"></div>

<div id="search-and-sort">
    <div style="overflow:hidden;">
        <input name="searchBar" id="searchBar" placeholder="Search"/>
    </div>
    <div class="btn-group">
        <span id="sortRecent" class="btn sorting">Sort by Most Recent</span>
        <span id="sortOldest" class="btn">Oldest</span>
        <span id="sortAuthor" class="btn">Author</span>
        <span id="sortTitle" class="btn">Title</span>
    </div>
    <div style="clear:both;"></div>
</div>

<div id = "itemList">
    {% assign chapters = site.pages | where: "layout", "chapter" | sort:'date' | reverse %}
    {% assign chapters = chapters | where: "name", "index.md" %}
    {% for chapter in chapters %}
      <div class = "item">
        {% include chapter.html chapter=chapter %}
      </div>
    {% endfor %}
</div>

<div class="top-border"></div>

{% include search-filter.html %}
