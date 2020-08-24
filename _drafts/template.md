---
layout: post # You generally won't want to change this.
title: "Template" # This is the title that'll appear on the page and on Google
category: landscape-analysis # Categories are reports. Use the file name (minus the .md)
tags: cengage # Tags are topics. Use the file name (minus the .md)
description: "The purpose of this document is to build on the Landscape Analysis by offering a roadmap of potential actions that stakeholders can use to chart both individual and collective responses." # This shows up in the sidebar, and on Google!
permalink: /template # This is the link it'll show up at.
pdf: "https://osf.io/preprints/lissa/2pwft/download" # if you have a pdf for the post put this here and it'll be used for the print button

# RARELY USED
hidden: true # exclude a post/page from pagination
date: 2019-03-29 03:00:00 # This date will override the date in the file name. Mainly we use it to handle ordering in reports / threads. The date can be the day the report was published, and the time can be used to sort posts.
authors: # This can be used to specify authors as below. This will change what the author box does. If you don't give any authors it'll use Claudio and SPARC, and you can delete this.
#  - claudi
#  - nicole
#  - raym
#  - heather
#  - joe
#  - nick
featured: true # This will make it turn up at the top of threads
homepage_latest: true # This will add it to the homepage’s "Latest Analysis" section 

# FOR LINK ONLY POSTS
link: https://sparcopen.org/news/2020/qa-cengage-mcgraw-hill-merger-one-year-and-counting/ # If you're doing a link only post, put the link here. Otherwise, delete this.
reading-time: 5 mins read # This manually sets the reading time on link only posts. If you are doing a link-only post delete this.
---

This page is for testing and demonstrating all the different types of content we'll use.

## Large header, `<h2>`
### Still big header, `<h3>`
#### Small header, `<h4>`
##### Smaller header, `<h5>`
###### Smallest header, `<h6>`

Don't use H1. It's too big.

[I am a link](https://yoururl.org)
*I am italic*
**I am bold**
<span class="pullquote">This is a really nice and pretty pull quote.<span>
I have a footnote[^1].
> I'm a block quote that can be used to quote ourselves previously

This is a line break, or `<br/>`
Created by inserting two spaces and a return

Insert a _Join SPARC_ infobox anywhere in the text like below (make sure that there is no extra indentation or spaces before):

{% include join-box.html %}

---

## Lists

Time for a list:

* this
* is
* an
* unordered list

and another list

1. this
2. list
3. has
4. numbers

---

## Logo (image needs love)

The logo is an inlined SVG image:

{% include svg/logo.svg %}

---

## Table (table needs love )

| Header      | Header      | Header      | Header      |
| ----------- | ----------- | ----------- | ----------- |
| Data        | Data        | Data        | Data        |
| Data        | Data        | Data        | Data        |
| Data        | Data        | Data        | Data        |
| Data        | Data        | Data        | Data        |

---

## Graphic

![Alt text explaining what this image represents]({{ site.BASE_PATH }}/media/figures/open_data_infrastructure.png)

***


[^1]: This is the first footnote.
