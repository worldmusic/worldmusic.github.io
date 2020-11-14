---
layout: default
title: Resources
description: Other useful resources from across the internet
---
One of our goals is to provide links to some of the many open and online resources that are related to the teaching and study of music. These are not exhaustive, but may provide starting points for research or reading. They are not meant to stand alone and, in some cases, require significant introduction and contextualization in the classroom.

Items labeled "Teaching" and some others (like "Virtual Fieldwork") are primarily intended for instructors. Others are resources that people have used as assigned reading/watching/listening in their undergraduate classrooms.

Please note that these items do not go through the same review process as *World Music Textbook* contributions. If you would like to add any resources, suggest a bibliography, have any concerns about a resource, would like to edit or add to a resource description, or find a broken link, please email [the editors](mailto:{{ site.email }}).

## Filter by Tag

<div id = "tagList"></div>

## Resources

<div id = "itemList">
    {% for bib in site.resources %}
        {% assign sorted-pubs = (bib.resources | sort:'date' | reverse) %}
        {% for pub in sorted-pubs %}
            <div class = "item">
                {% include item.html pub=pub %}
            </div>
        {% endfor %}
    {% endfor %}
</div>

{% include tag-script.html %}
