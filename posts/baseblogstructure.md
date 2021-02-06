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
Eleventy transforms a directory of templates (of varying types) into HTML. It deploys to Netlify.

The templates it supports are: Liquid, Nunjucks, Handlebars, HTML, Markdown, EJS, Haml, Pug, Javascript

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
    <table class="table table-hover table-bordered border-primary vertical-align-middle">
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
                <td>css</td>
                <td><table><tbody>
                        <tr><td>index.css</td></tr>
                        <tr><td>prism-base16-monokai.dark.css</td></tr>
                    </tbody></table>
                </td>
                <td><table><tbody>
                        <tr><td>css for blog pages</td></tr>
                        <tr><td>css for how code should look</td></tr>
                    </tbody></table>
                </td>
            <tr>
        </tbody>
    </table>
</div>
