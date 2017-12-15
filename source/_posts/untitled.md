---
date: 2017-12-09 16:51:40
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

## *This post has no title whatsoever* ##

This is the ninth in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This test *post has no title*.  The test is to confirm that the post remains accessible.

This test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) `no-title.md` Post of 2013-12-25.  

## Code ##

```
---
date: 2017-12-09 16:51:40
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

The challenge is to see how the post remains accessible, how it appears in archives and the Recent Post lists, and how it is separated from others on the index page.

## Observations ##

 * The persistent post has its slug specified as "`untitled`" and is located at [wingnut/2017/12/09/untitled](http://orcmid.com/BlunderDome/wingnut/2017/12/09/untitled/).  In archives and archive-like indexes, there is no title, only a post date.  
 
 * The persistent post can be located from other locations and index entries by the post date.
 
 * It becomes interesting to know what happens if two no-title posts are produced on the same date.  
 
 * In the RSS feed, the post is given the first heading of the page as its title.  So some sort of title always appears in FeedDemon, and it links to the post article. *added 2017-12-14*
 
 * At the bottom of the post article where the Newer and Older article links appear, an untitled post at Newer is listed and linked as "(no title)."  In the Older position, there is no link and now text for an untitled post, bu the "Older" title will link to it.  *added 2017-12-14*
 


