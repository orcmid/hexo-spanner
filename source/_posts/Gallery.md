---
title: Hexo Unit Test - Gallery
date: 2017-12-04 14:41:34
photos:
- /2017/11/28/Test/wallpaper-2572384.jpg
- /2017/11/28/Test/wallpaper-2311325.jpg
- /2017/11/28/Test/wallpaper-878514.jpg
- http://placehold.it/350x150.jpg
categories:
- [Authoring, Markdown]
- [Blog Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- images
- Landscape Theme
- Markdown
- Observations
---
This is the fifth of a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This confirms special provision for a photo gallery at the beginning of a post.

This test requires relative addressing to particular folders of the public structure.  The unit-test Gallery uses the same photos as the [Wingnut Image Assets](http://orcmid.com/BlunderDome/wingnut/2017/11/28/Test/) post and they are used from that post's asset folder.

The test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) "Gallery" test post of 2013-12-25.

## Code ##

The gallery is specified in the front matter here.

```
--
title: Gallery
date: 2017-12-04 14:41:34
photos:
- /2017/11/28/Test/wallpaper-2572384.jpg
- /2017/11/28/Test/wallpaper-2311325.jpg
- /2017/11/28/Test/wallpaper-878514.jpg
- http://placehold.it/350x150.jpg
categories:
- [Authoring, Markdown]
- [Blog Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- images
- Landscape Theme
- Markdown
- Observations
---
```

## Gallery Viewing ##

The first of the four photos shows automtatically above the title of the post page. 

To view the gallery images, click on the one shown.  The fancibox image window will pop out.  Inside the right/left edges of the current photo pointers will appear, enabling cycling through the four images.

- Widescreen wallpaper of a cat
- Portrait orientation photo of a girl in a fruit collage
- very wide and narrow widescreen wallpaper
- smaller photo of a placeholder image

All photos should be displayed properly.

*From [Wallbase.cc](http://wallbase.cc)*

## Observations ##

 * The gallery and images are not reflected in the RSS Atom feed of a gallery page.  This is another reason for avoiding this feature where an RSS record is important.  *added 2017-12-14*

 * The gallery view has each image fit within the browser-window.  Resizing can be used to provide larger or smaller views.
 
 * It is unclear to me whether there is much use of this in nfoCentrale blogs.  Part of it has to do with the absence of captions and of any indication that a gallery is being provided.  
 
 * Because the assets location must be known, it takes a little work to get the front-matter set up.  That's not difficult, but requires iterative creation and viewing of a gallery post.
 
 * It seems desirable to have a special gallery scaffold page.  That might provide some recuring information in having the visitor understand that there is a gallery.
 
 * I notice that, with the default landscape theme setup, if there are individual images on a page, they each pop-out as their gallery page, and the other images are in a gallery that can be cycled through from any of the pop-outs. *added 2017-12-05*
  
