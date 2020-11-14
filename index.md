---
layout: default
title: "World Music Textbook"
description: "An online and open resource for teaching and <br>learning ethnomusicology and musicology"
---
The *World Music Textbook* is a new collaborative effort to create a free and broadly accessible resource for the general public, educators, students, and researchers alike. Its open collections of scholarly, peer-reviewed writing and multimedia materials will focus on increasing access to underrepresented voices, writing styles, and audiences, all with undergraduate students and a broad readership in mind.

<center>
  <a href="{{ site.baseurl }}/about" class="btn">Learn more about the project</a>
  <a href="{{ site.baseurl }}/about" class="btn">Call for contributions</a>
</center>

## News and updates

About recent articles, news, and so on.

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

!["Musician busking"](assets/images/william-recinos-nola-violin-unsplash.jpg)
<small>*"Musician busking" by William Recinos on [Unsplash](https://unsplash.com/@iwillbmm)*</small>

## Recently published chapters

<div id = "itemList">
    {% assign chapters = site.pages | where: "layout", "chapter" | sort:'date' | reverse %}
    {% for chapter in chapters limit:3 %}
      <div class = "item">
        {% include chapter.html chapter=chapter %}
      </div>
    {% endfor %}
</div>

<div class="top-border">
<p>
<center>
  <a href="{{ site.baseurl }}/chapters" class="btn">See all chapters</a>
  <a href="{{ site.baseurl }}/resources" class="btn">Other resources</a>
</center>
</p>
</div>
