---
title: Hexo Unit Test - Link
date: 2017-12-07 19:47:50
link: https://www.bing.com/
categories:
- [Authoring, Markdown]
- [Bloc Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Markdown
- Observations
- TODOs
---
This is the sixth in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This confirms operation of a special provision for a post that establishes a link in its Front Matter.

This test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) "Link Post" of 2013-12-24.

Clicking on the title of the post will should open [Bing](https://www.bing.com) in a new tab or window.  Click on the date instead to get to the archive location of the post.

## Code ##

The link specification is in the front-matter.

```
---
title: Hexo Unit Test - Link
date: 2017-12-07 19:47:50
link: https://www.bing.com/
categories:
- [Authoring, Markdown]
- [Bloc Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Markdown
- Observations
- TODOs
---
```

## Observvations ##

 * I don't see any way to use this.
 
 * Since clicking on the title is the standard way to access the single-page of a post, having that link go elsewhere sometimes strikes me as misleading.  
 
 * It is very subtle that the date links to the single-page of the post.  I need to make two posts on the same day and confirm that is actually what happens.
 
