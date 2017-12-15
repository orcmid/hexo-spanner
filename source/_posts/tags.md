---
title: Hexo Unit Test - Post Tags
date: 2017-12-12 08:32:56
categories:
- [Authoring, Markdown]
- [Blog Development, Hexo, landscape theme]
- [Blog Development, Hexo, tags]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Markdown
- Observations
- TODOs
- tags
---

This is the eleventh in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This test is the Wingnut counterpart of the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) `tags.md` post of 2013-12-24.

The test involves introduction of three tags in the front matter. 

```
tags:
- Foo
- Bar
- Baz
```

I do not wish to add tag entries on the sidebar and in the archives for those useless tags.  Tags are already working and this is just a place-holder confirmation.  Here, the front matter has used tags along with other material.

## Code ##

```
---
title: Hexo Unit Test - Post Tags
date: 2017-12-12 08:32:56
categories:
- [Authoring, Markdown]
- [Blog Development, Hexo, landscape theme]
- [Blog Development, Hexo, tags]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Markdown
- Observations
- TODOs
- tags
---
```

## Expected Result ##

The effect will be to list the tags at the bottom of the post.  

{% asset_img wingnut-BottomTags.png "post-bottom tags strip" %}

In addition, those tags will be listed among the TAGS sidebar listing. 

{% asset_img wingnut-SidebarTags.png "Sidebar tag list" %}

Both listings have clickable tag names, providing an archive-style list of those posts that use the tag, including this one.

## Observations ##

 * The post-bottom list of tags is unobtrusive, and the small type is also valuable.  For long posts, this material is not easily come by.
 
 * Confirmation of the unit test requires verification that the post on the home page and at the permanent post location have the tags listing at the bottom of the page body.  
 
   * Each body entry for a tag must link to an archive-style page of all current posts that employ the same tag.
  
   * The sidebar entry for TAGS should have links in the same manner.
 
 * The screen captures are based on the landscape features as they are rendered as of 2017-12-12.  Later updates to some features may have this post appear differently.
 
 * It is unfortunate that changes to the sidebar cause all pages to be regenerated.  It changes the sense of "Recent Posts" although it does keep the sidebar Categories and Tag lists current.  I would prefer something different, if I could figure out what that might be and how to introduce it.
 
 * If tag maps were being used, it would be nice for those to be reflected on every page as the lastest.  This suggests to me that this should be generated at server access time, from stored data.  That changes how much on the site has to be regenerated, and might not be too intrusive.  That does sound like considerable effort and it changes the static character of the blog.  A quandary.
 
 * In the RSS feed, the specified tags (and categories) are recorded.  The read feeder need not provide anything for them.  There is nothing available using FeedDemon. *added 2017-12-14*
 
