---
layout: default
title: "World Music Textbook"
description: "An online and open resource for teaching and <br>learning ethnomusicology and musicology"
---

The _World Music Textbook_ is a new collaborative effort to create a free and broadly accessible resource for the general public, educators, students, and researchers alike. Its open collections of scholarly, peer-reviewed writing and multimedia materials focus on increasing access to underrepresented voices, writing styles, and audiences, all with undergraduate students and a broad readership in mind.

<center>
  <a href="{{ site.baseurl }}/call" class="btn">Call for contributions</a>
  <a href="{{ site.baseurl }}/about" class="btn">About the project</a>
</center>

## Recently published chapters

<div id = "itemList">
    {% assign chapters = site.pages | where: "layout", "chapter" | sort:'date' | reverse %}
    {% assign chapters = chapters | where: "name", "index.md" %}
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

!["Musician busking"](assets/images/william-recinos-nola-violin-unsplash.jpg)
<small>_"Musician busking" by William Recinos on [Unsplash](https://unsplash.com/@iwillbmm)_</small>

## News and updates

### And we're off!

We are proud to share [our first contributions]({{ site.baseurl }}/chapters/) and an [extended resource listing]({{ site.baseurl }}/resources/). We invite scholars, musicians, and community members to submit materials for inclusion and continue to accept contributions on a rolling basis.

You can follow us on [Twitter](https://twitter.com/music_textbook) and [Facebook](https://www.facebook.com/WorldMusicTextbook) for updates on the project and to learn about newly published contributions.
