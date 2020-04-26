---
title: "Writing a blog post"
weight: 10
---

# Introduction

Writing a blog post for the CogSite is very simple.
You basically just have to write the blog post in
markdown (which you can read about how to do
[here](writing-in-markdown)), upload the images
along with your blog post, and send a pull request
so it can be incorporated into the main website!

Here you can read about the specifics of writing the blog posts and what is relevant to think about when writing the blog posts.

# Blog page settings

Below is an example of specific pages settings (see [page settings](page-settings) for the other page settings):

```
author: "Esben Kran"
date: 2020-04-22
linktitle: Writing in markdown
menu:
  main:
    parent: tutorials
next: /next-blog-post-name-with-hyphens
prev: /previous-blog-post-name
```

The author and date are pretty self-explanatory. The linktitle is a way to shorten writing the link to this post but is usually not relevant.

The menu is possibly not relevant but gives you access to not automatically index the blog posts. They are currently not supported. The menu "main" is set in the (blog header)[#blog-header].

The next and prev are two buttons at the bottom of the blog post you are writing that specify links to other blog posts that are relevant to have as the next and the previous in relation to this.

# Blog header

The header of the .md (markdown) file you use to write a blog post has some settings specific to blog posts (see [page settings](page-settings) for general page settings). Below is an example of such settings:

```
+++
title = "Writing a blog post"
description = "How to submit a blog post for the CogSite"
tags = [
    "crowdsourcing",
    "knowledge",
]
date = "2020-04-22"
categories = [
    "contribution",
]
menu = "main"
+++
```
