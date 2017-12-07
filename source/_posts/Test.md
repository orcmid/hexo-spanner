---
layout: theme
title: Hexo Unit Test - Wingnut Image Assets
date: 2017-11-28 16:04:06
updated: 2017-12-03 16:46:00
categories:
 - [Authoring, Markdown]
 - [Blog Development, Hexo, landscape theme]
 - [blogs, Spanner Wingnut]
tags:
 - Hexo 
 - Landscape Theme
 - Markdown
 - Images
 - Observations
 - TODOs
---

This is the first of a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This confirms basic support for inclusion of images in posts on the blog.

This test verifies image inclusion from a post-specific asset folder, the folder that has the generated post/page as its index.html.  The test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) "Image" test post of 2013-12-26.

#### Code ####

The original code is

```
![](/assets/wallpaper-2572384.jpg)

![Caption](/assets/wallpaper-2311325.jpg)

![](/assets/wallpaper-878514.jpg)

![Small Picture](http://placehold.it/350x150.jpg)
```

For Spanner Wingnut, there is no common assets folder at the blog location.  Instead, the three local test images are moved to the `spanner/source/_posts/Test/` folder, corresponding to the `spanner/source/_posts/Test.md` file that has the source text of this blog post.

To use those assets properly, the code becomes

```
{% asset_img wallpaper-2572384.jpg "1920 x 1200 kitten" %}

{% asset_img wallpaper-2311325.jpg "1383 x 1858 fruit cup girl !?" %}

{% asset_img wallpaper-878514.jpg "3840 x 1200 waterfront cityscape" %}

![350 x 150 gray "placeholder" block](http://placehold.it/350x150.jpg)
```

No provision for positioning, scaling or anything else is included.  The test is for minimal and simple inclusion of images.

For an existing rendition of the test, see the [Theme Anatole Demo Images page](anatole.munen.cc/2016/12/26/images/).

#### Resulting Images ####

{% asset_img wallpaper-2572384.jpg "1920 x 1200 kitten" %}

{% asset_img wallpaper-2311325.jpg "1383 x 1858 fruit cup girl !?" %}

{% asset_img wallpaper-878514.jpg "3840 x 1200 waterfront cityscape" %}

![350 x 150 gray "placeholder" block](http://placehold.it/350x150.jpg)

Note the captions.  They are also the mouse-over titles.  Also, the images are all sized to the article width.  The Fancybox pop-out view can be seen by clicking on individual images.  Resizing the blog page allows the higher-resolution pop-out images to expand to their full resolution.  Try that on the cityscape.

#### Observations ####

 * Specify links in images - I suppose in the captions if fancybox is kept.
 
 * Specify position, sizings, and margins in some straightforward manner
 
 * Specify Alt Text
 
 * Have better formatting for the Captions/Titles.
 
 * Find out how to accomplish this with parameters on `{$` items or find appropriate HTML tagging to apply when these matter.  I definitely want to operate with post-specific assets and not global ones.
 
 That's all for now.
 
 > *update 2017-12-03* Adjust categories/tags and observations.
