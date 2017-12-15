---
title: Hexo Unit Test - Categories
date: 2017-12-02 17:56:02
updated: 2017-12-04 22:18:00
categories:
- [Blog Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
- [Toolcraft, JavaScript, NodeJS]
- [Authoring, Markdown, HTML, CSS]
- Golden Geek
tags:
- Categories
- TODOs
- Observations
- Hexo
---
This is the fourth in a series of Spanner Wingnut confirmation tests based on the Hexo Unit Tests for Themes.  This version demonstrates the establishment of five categories, four of them nesting others.  Part of this test is to confirm exactly how that is intended to work.

This test is the wingnut-specific counterpart of the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test)  "Categories" test post of 2013-12-24.

## Original Markdown ##

Categories are specified in the front-matter at the beginning of the post's markdown.

```
---
title: Hexo Unit Test - Categories
date: 2017-12-02 17:56:02
updated: 2017-12-03 15:43:00
categories:
- [Blog Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
- [Toolcraft, JavaScript, NodeJS]
- [Authoring, Markdown, HTML, CSS]
- Golden Geek
tags:
- Categories
- TODOs
- Observations
- Hexo
---
```

## Observations ##

 * The established categories will be extended as needed for further posts.  How this works and the use of category maps remains to be understood.

 * The appearance of the category list between the date of a post and its title deserves refinement.
 
 * When other blogs are restored, categories and tags should be operating from the beginning.
 
 * The impact of using the "updated" property in the front-matter needs to be understood.  Perhaps related to RSS feed updating?
 
 * There is too much use of very light small caps items, and the light date on posts.  Along with major features that require work and testing, these touch-ups will be important for the legibility and personality of nfoCentrale blogs.
 
 * <strike>For the record, it is worthwhile to review posts so far and introduce tags and categories.</strike> *done 2017-12-03*
 
 * Categories are touchy.  It is possible to create peers at the same level
   (e.g., in the [blogs](http://orcmid.com/BlunderDome/wingnut/hexo-categories/blogs/) category).  <strike>However, changes in a categories of a post are not detected and defects will be preserved.  I am looking at how to trigger post and category tree regeneration. *added 2017-12-08*</strike> When fixed in the front matter, category changes are detected and reflected.  Deletions will remain on the hosted site until explicitly removed, but not serious. *updated 2017-12-08*
   
 * Categories (and tags) are reported in the RSS feed, although the FeedDemon reader does not make use of them.  **added 2017-12-14**

> *updated 2017-12-03* to correct a heading, add tags, and record observations 



