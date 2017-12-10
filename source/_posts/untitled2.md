---
date: 2017-12-09 17:13:11
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

## *This post also has no title whatsoever* ##

This is the tenth in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This test is the second one produced on this day with no title.

This test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) `no-title.md` Post of 2013-12-25.  

## Code ##

```
---
date: 2017-12-09 17:13:11
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

The challenge is to see how the post remains accessible, how it appears in archives and the Recent Post lists, and how it is separated from others on the index page.  For this case, it is about two no-title pages produced on the same day.

## Observations ##

 * The persistent post has its slug specified as "`untitled2`" and is located at [wingnut/2017/12/09/untitled2](http://orcmid.com/BlunderDome/wingnut/2017/12/09/untitled2/).  In archives and archive-like indexes, there is no title, only a post date.  
 
 * The persistent post can be located from other locations and index entries by the post date.
 
 * In Recent Posts, the post is identified as "(no title)".  In archive and archive-like lists, there is only the date, and the two untitled posts for December 9, 2017, each have a date-only entry.
 
 * There is not much to complain about.  The edge case works well enough.  If convenient, it might be handy to use the (no title) designation in archive-like lists as well.
 
 * I'm declaring relief that all of the title tests have been produced.  Now to move on to other features.


