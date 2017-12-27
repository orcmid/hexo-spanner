---
title: videos
date: 2017-12-26 08:11:36
updated: 2017-12-27 00:45
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
- videos
---
This is the twelfth in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This test is the Wingnut counterpart of the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) `videos.md` post of 2013-12-25.

## Tests##

The first two videos are from the original unit test:

```
### YouTube 1 ###

{% youtube TIbZDRXM-Tg %}

## Vimeo test ##

{% vimeo 82090131 %}
```

### YouTube 1 ###

{% youtube TIbZDRXM-Tg %}

### Vimeo test ###

{% vimeo 82090131 %}

These confirm that the specified tests run.  The video markdowns are described in the [Tag Plugins](https://hexo.io/docs/tag-plugins.html) documentation.  These two tests confirm those plugins are available and active.

The next confirmation is with a video of the kind that is important for me to share.

```
{% youtube XmsCaN0bH1k?t=20m54s %}
```

is part of an important address by Edward Ashford Lee at a panel on [Living in the Cyberworld](https://www.youtube.com/watch?v=XmsCaN0bH1k).  All of the discussion is important.  I am featuring, here, a segment on the reconciliation of scientific and engineering approaches around models.  Althoug models of computation are not scientific models in the same sense that models of nature are, the relationship between mathematical models, engineering, and the incredible layering of abstractions on which dependable computing rests deserves careful attention.

{% youtube XmsCaN0bH1k?t=20m54s %}

Start about 20 minutes in and watch at least through to the point where programming languages are placed atop an extraordinary layering of abstraction beyond single transistors.  

Edward Lee's address ends at the 30-minute mark.  The subsequent remarks and panel discussion are also informative.  You will see there that non-determinism is used in more than one sense in discussions around non-deterministic models of systems.

## Observations ##

 * All of the tests work.  Note that YouTube cookies can influence where the YouTube videos begin on a second viewing.
 
  * Attempting to start a YouTube video at a preset time marker apparently doesn't work with the youtube tag plug-in.  This needs to be researched.
  
  * For some reason, refreshing the page has the first YouTube video frame appear for the second, Vimeo, frame as well.  This occurs when viewing via Microsoft Edge 41.16299.15.0.
  
  

