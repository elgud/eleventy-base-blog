---
title: Thoughts on the JAMstack
description: The jamstack course is finished. I reflect on what I have learnt and the questions I still have and what I still need to find out.
date: 2021-04-13
tags:
  - jamstack
  - eleventy
  - static site generators
  - CMS
  - netlify
layout: layouts/post.njk
---

## What is the JAMStack?
The 'JAM' part of JAMStack stands for Javascript, API and Markup. Markup means HTML with which you create the structure of a webpage. Javascript provides interaction within a page. I have used Javascript to allow the user to calculate factorials, triangle and pyramidal numbers. The final Javascript exercise was to create a gallery of 4 types of animal and to provide buttons and a search facility to filter which images are shown. I am to create filter functionality for the home page based on this.

The CMS (Content Management System) that we attached to our sites is a single admin page written in Javascript.

The A in JAM stands for API or Application Programming Interface. We did not really the API part in action during the course and this begs some questions. We used Netlify to host our sites and Netlify provided the backend for the forms so you can see and download form submissions. Netlify also provided functionality connected to GitHub so that you simply commit your changes to GitHub and Netlify automatically recompiles your site and hosts it. Note that the contents of _site are not committed to GitHub.

The stack is the combination of web technologies that you use in order to create your website. 

## What are the advantages of the JAMStack
A key part of the JAMStack is the use of a 'static site generator' which pre-compiles your code into a static site that consists of html, css, and javascript. Eleventy is an example of a static site generator. It takes a collection of html, markdown, and nunjucks files and compiles them into a simple site that consists of html, css, and javascript. The compile part assembles the webpages. Markdown and nunjucks allows you to separate content from the structure of the site to a certain extent. So the parts that are common to all pages are specified in a separate file and added to the content at compile time.

Nunjucks also enables you to use programming constructs such as loops to create your html. This means that if you want to make changes, you change just one bit of code instead of lots of separate bits of html. 

But the big advantage of pre-compiled code is that the code is not compiled when someone accesses your site. This means that pages can be served to users more quickly.

Because the site is pre-compiled maintenance is easier. You no longer have to do continual updates to the underlying software. The only maintenance is content creation and changing the content. If you do nothing, the site will just sit there. There is no more regular updating of the underlying technology behind the site. This is great for static sites.

## Separation of front end and back end
A much touted advantage of the JAMStack is the separation of the front end and the back end. The JAMStack compares itself with software such as Wordpress (and Concrete5, which is what I use) which handles both the display of the site and backend function such as dealing with users and handling form submission.

The problem is that although with the JAMStack, you have a lot of freedom to mix and match static site generators and content management systems as you wish. It is not clear where the backend functions such as form submission and dealing with users comes from. It is also not clear how to go about hosting the resulting site short of simply copying the compiled result to your hosting server. The latter could get very tedious if most or all of the files have to be copied for a relatively small change.

## Hosting
A search for JAMstack hosting does not reveal many:
- Netlify
- Vercel
- Cloudfare Workers Sites
- Amazon Web Services
- Firebase (Google)

So it could be difficult to host on a stand cpanel hosting provider. What worries me about the above list is it consists mainly of the big internet players. 

I attended part of a training session on the JAMStack by Netlify. While this did contain some useful information, it was very much a session on selling Netlify. I am not sure it is a good idea to be tied to one hosting provider. Netlify offers a lot for free, but the cheapest paid plan is quite expensive at $19 per 'member' per month. If you wnat role based access control, then it is $99 per month.

## Conclusion
The JAMStack looks good. I certainly like the idea of precompiling pages. But there are still questions and many things to try out. My current hosting provider does do node.js projects, so it may be possible to compile an eleventy site on it. I just do not know.

The lack of obvious backend solutions without going for either specialist or large hosting providers bothers me.


