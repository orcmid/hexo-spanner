---
title: Hexo Unit Test - Excerpts
date: 2017-12-01 12:02:33
updated: 2017-12-03 16:26:00
categories:
 - [Authoring, Markdown]
 - [Blog Development, Hexo]
 - [blogs, Spanner Wingnut] 
tags:
 - Hexo 
 - Markdown
 - HTML comments
 - Excerpts
 - TODOs
 - Observations
---

This is the third in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This test demonstrates how a post can be restricted to an exerpt on the front page of the blog, with the full post in the by-date permanent location of the post.

<!-- more -->

This test is based on the [Hexo Theme Unit Test](https://github.com/hexojs/hexo-theme-unit-test) `excerpts.md` test file.  When implemented, it has a "read more" link and the remainder of the post page is only visible on the archive version, not on the front-page of the blog.

It is not necessary to activate the use of explicit excerpts.  This test confirmst that.  I can do that whenever it is ever important.

One complication in explaining this text is that the break point after the intended excerpt is via HTML comment, so it could be difficult to exhibit, in the page, the MarkDown that demarks the separation between exerpt and the full body of the post. 

```
<!-- more -->
```
** Observations ** 

 * The processor of code blocks has been done in a way that there is no accidental leaking of HTML-interpreted elements.  Another one of those nice touches that has me smile.

 * The "Read More" link goes to a continuation point (`#more`) in the body of the complete post.  This is a bit distracting.  Consider just going to the top.  On the other hand, it is unlikely that Excerpts will be used.
 
 * The only interest in exerpts is to assure that the facility is working properly.  It is unlikely that it will be used for nfoCentrale blogs.
 
> *update 2017-12-03* Added observations and made categories/tags adjustments
