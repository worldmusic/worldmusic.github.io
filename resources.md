---
layout: default
title: Resources
description: Other useful resources from across the internet
permalink: /resources/
nav:
 - "home"
 - "call"
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

<script>

// collect tags for the filter list
var tagElements = document.getElementsByClassName("tag");
var tagList = document.getElementById("tagList");
var tags = [];

for (i = 0; i < tagElements.length; i++) {
    if (tags.indexOf(tagElements[i].innerText) < 0) {
        tags.push(tagElements[i].innerText);
    }
}

// create buttons for the filter list
tags.sort();
for (i = 0; i < tags.length; i++) {
    var button = document.createElement("span");
    var text = document.createTextNode(tags[i]);
    button.appendChild(text);
    button.classList.add("tag");
    button.classList.add("filter");
    button.classList.add("btn");
    tagList.appendChild(button);
}

// set events for filter list
var active = [];

var filters = document.getElementsByClassName("filter");
var items = document.getElementsByClassName("item");
for (i = 0; i < filters.length; i++) {
    let e = filters[i];
    e.addEventListener("click", function() {

        // change button status and create list of active tags
        if (e.classList.contains("active")) {
            e.classList.remove("active");
            active.splice(active.indexOf(e.innerText), 1);
        }
        else {
            e.classList.add("active");
            active.push(e.innerText);
        }

        // hide and show items
        if (active.length == 0) {
            for (j = 0; j < items.length; j++) {
                items[j].style.display = "block";
            }
        }
        else {

            // get item tags and check that each one is active
            for (j = 0; j < items.length; j++) {
                let itemTags = items[j].getElementsByTagName("span");
                let matches = 0;
                for (k = 0; k < itemTags.length; k++) {
                    if (active.indexOf(itemTags[k].innerText) >= 0) {
                        matches++;
                    }
                }

                // show or hide
                if (matches >= active.length) {
                    items[j].style.display = "block";
                }
                else {
                    items[j].style.display = "none";
                }
            }
        }
    })
}
</script>
