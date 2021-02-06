---
title: Structure of Eleventy Base Blog
description: An exploration of the file structure of the Eleventy Base Blog
date: 2021-02-07
tags:
  - file-structure
  - eleventy-base-blog
layout: layouts/post.njk
---

## Eleventy
Eleventy transforms a directory of templates (of varying types) into HTML It deploys to Netlify.

The templates it supports are: Liquid, Nunjucks, Handlebars, HTML, Markdown, EJS,Haml, Pug, Javascript

The Eleventy [website](https://www.11ty.dev) is https://11th.dev
[Documentation](https://www.11ty.dev/docs) is at https://www.11ty.dev/docs though these are of limited help if you do not know the template technology in the above list.

There is some information in README.md

The templates used in the base blog are Markdown (.md) and nunjucks (.njk).

eleventy.js has config information. This says
- The template formats used are md, njk, html, and liquid
- The markdown template engine is liquid
- The html template engine is nunjucks (njk)
- The data template engine is nunjucks (njk)

nunjucks is a templating language for javascript, written my [mozzilla](https://www.mozilla.github.io/nunjucks)

liquid is a template language created by shopify. It is written in Ruby adn is used by many other web apps including jekyll (which is used by GitHub).

Eleventy base blog also makes use of json.

## The folder _site
_site is not included in the git changes. It gives a good starting point for working out what the code actually does. _site contains the following directories:

<div class="table-responsive">
    <table class="table table-hover table-bordered border-primary align-middle">
        <thead>
            <tr>
                <th>folder</th><th>files</th><th>comment</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>about</td><td>index.html</td><td>the about page</td>
            </tr>
            <tr>
                <td rowspan="2">css</td>
                <td>index.css</td><td>css for blog pages</td>
            </tr>
            <tr>
                <td>prism-base16-monokai.dark.css</td>
                <td>css for how code (```) should look</td></tr>            
            </tr>
            <tr>
                <td rowspan="3">feed</td>
                <td>.htaccess</td><td>.htaccess file</td>
            </tr>
            <tr>
                <td>feed.json</td><td>json file of contents of whole site</td>
            </tr>
            <tr>
                <td>feed.xml</td><td>xml file of contents of whole site</td>
            </tr>
            <tr><td>img</td><td>.gitkeep</td><td>.gitkeep is empty</td></tr>
            <tr><td>page-list</td><td>index.html</td>
                 <td>table of all pages with their links and titles</td>
            </tr>
            <tr><td rowspan="5">posts</td><td>index.html</td>
                <td>Archive page: list of blog posts with links</td>
            </tr>
            <tr>
                <td>firstpost/index.html</td>
                <td rowspan="4">pages each containing a blog post</td>
            </tr>
            <tr><td>secondpost/index.html</td></tr>
            <tr><td>thirdpost/index.html</td></tr>
            <tr><td>fourthpost/index.html</td></tr>
            <tr><td rowspan="4">tags</td><td>index.html</td>
                <td>A page showing a list of tags in button format to click. Clicking takes you to the appropriate page below.</td>
            </tr>
            <tr><td>another-tag/index.html</td>
                <td rowspan="3">A list of blog posts with the tag in question.</td>
            </tr>
            <tr><td>number-2/index.html</td></tr>
            <tr><td>second-tag/index.html</td></tr>
        </tbody>
    </table>
</div>

Then there are three single files in _site:
<div class="table-responsive">
    <table class="table table-hover table-bordered border-primary align-middle">
        <thead>
            <tr>
                <th>file</th><th>comment</th>
            </tr>
        </thead>
        <tbody>
        <tr><td>404.html</td><td>Page/Content not found error page</td></tr>
        <tr><td>index.html</td><td>home page</td></tr>
        <tr><td>sitemap.xml</td><td>list of urls of all pages in site with their last modified date in xml format.</td></tr>
        </tbody>
    </table>
</div>
<tr><td>posts.json</td>
                <td>template for matching tags to posts?</td>
