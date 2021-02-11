---
title: Collections in Eleventy 
description: How the collections in Eleventy work and how to create a new set of pages that act like the blog posts but are separate from them.
date: 2021-02-06
tags:
  - add-post
  - delete-post
layout: layouts/post.njk
---

Basically, all pages are added to collections. You can access all of them using collections.all (see sitemap.xml.njk).

Where there are tags, you can access a sub-collection of tags via collections.tag-name. So to create a group of pages you give them all the same tag (example in your case).
The posts.json file simply adds the tag of 'post' to all the .md files in the directory. Looking at the posts in posts directory none have an explicit tag of post because this is added by posts.json.  Therefore they can be accessed via collections.posts.

The file pastelists.njk in _includes that we were wondering about is generic code to display a list of pages associated with a tag. So archive.njk sets a variable called postslist and passes this too postlist.njk by including the code from postlist.njk. So you can write an alternative archive.njk that sets variable postslist to collections.tag-name.


