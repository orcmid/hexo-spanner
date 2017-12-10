---
title: Hexo Unit Test - Long Title Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam justo turpis, tincidunt ac convallis id.
date: 2017-12-09 16:07:37
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
This is the eighth in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This simply demonstrates how a long title is handled.

This test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) `long-title.md` Post of 2013-12-24.  

## Code ##

```
---
title: Hexo Unit Test - Long Title Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam justo turpis, tincidunt ac convallis id.
date: 2017-12-09 16:07:37
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

 * Review how the title appears in Recent Posts, Archives, and the categories and tag archive-index-like pages.  

 * Also check how the responsive formatting is handled as the browser window is narrowed or a mobile device is used.

 * It is great for this to work.  Keeping titles appropriately short is preferable, of course.
 
 * I want to adjust the Recent Posts list so that continuations on multiple lines are set off.  I think using an unnumbered list will do the job best.
 
 * The entire blog is regenerated too often.  I need to determine which features can be adjusted (such as the Categories and Tags sidebar, maybe) to inhibit this.  As my blogs become populated with thousands of posts, the regeneration will not be endurable, especially with the amount of material that is then synchronized.

