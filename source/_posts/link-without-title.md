---
date: 2017-12-09 10:01:43
link: https://www.bing.com/
categories:
- [Authoring, Markdown]
- [Blog Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Markdown
- Observations
- TODOs
---
This is the seventh in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This confirms operation of a special provision for a post that establishes a link in its Front Matter in the absence of a title.

This test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) `link-post-without-title.md` Post of 2013-12-24.  

Instead of a text title, the link itself should be presented. Clicking on that "title" should open [Bing](https://www.bing.com) in a new tab or window.  Click on the date instead to get to the archive location of the post.

## Code ###

```
---
date: 2017-12-09 10:01:43
link: https://www.bing.com/
categories:
- [Authoring, Markdown]
- [Blog Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Markdown
- Observations
- TODOs
---
```

## Observations ##

 * This is similar to the sixth unit test, "[Hexo Unit Test - Link](http://orcmid.com/BlunderDome/wingnut/2017/12/07/Link/)" except a form of the link is expected to appear in place of the missing title.
 
 * I find it odd that this front-matter link case occupies so much unit-test attention.  In this particular link-as-title case, there might be some usefulness.  
 
 * I remain concerned that the collision of two different link cases for titles is awkward and defeats confident usability.
 
 * It is also important to check how this form of post is listed in the archives and in category and tag lists.  In this case, only the faux title appears and clicking there follows the link instead of finding the post itself.  This applies to the sixth unit test also.  (Clicking the date above the archive/category/tag title will find the post.)  
 
 * My conclusion is that this no-title link case is workable if there is no body to the post, only the front matter.  That minimizes confusion in the situation where all one wants to provide is a link.  It remains a borderline hostile act to omit any guidance that assists the reader's determination of the prospective benefit of following the link.
 
 * In the RSS feed, the title refers to the blog post and the link is not carried forward when viewed in FeedDemon.  This also makes the link case, with or without title, inconsistent in another way.  *added 2017-12-14*

