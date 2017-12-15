---
title: Wingnut Feature Activation - RSS Feed
date: 2017-12-15 08:40:24
categories:
- [Blog Development, Hexo, landscape theme]
- [Blog Development, Hexo, RSS feed]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- RSS Feed
- Observations
- TODOs
- tags
---

To enable creation of the RSS Feed, using the default `hexo install` and `landscape` theme, it is necessary to add the hexo-feed-generator plugin.

{% blockquote hexo-theme-landscape https://github.com/hexojs/hexo-theme-landscape/blob/master/README.md README.md  %}
**Landscape requires Hexo 2.4 and above.** If you would like to enable the RSS, the [hexo-generate-feed](https://github.com/hexojs/hexo-generator-feed) plugin is also required.
{% endblockquote %}

## Code ##

In `themes/landscape/_config.yml` there is one setting for RSS.  

{% codeblock "theme/landscape/_config.yml" lang:yml https://github.com/hexojs/hexo-theme-landscape "hexo-theme-landscape" %}
# Header
menu:
  Home: /
  Archives: /archives
rss: /atom.xml
{% endcodeblock %}

For Spanner Wingnut, the names are customized to avoid conflicts with side-by-side installation of older (and someday newer) editions of the blog.

{% codeblock "spanner/themes/landscape/_config.yml" lang:yml https://github.com/orcmid/hexo-theme-landscape-wingnut "hexo-theme-landscape-wingnut" first_line:22 %}
# Header
menu:
  Home: /
  Archives: /hexo-archives                                   # 0.0.5
  About: /hexo-about     # hat tip to John Stevenson         # 0.0.3         
rss: /hexo-atom.xml                                          # 0.0.6
{% endcodeblock %}

It appears that the `rss` property, there, is for the menu button rather than anything to do with generation of the feed.

In accordance with the [hexo-generator-feed](https://github.com/hexojs/hexo-generator-feed) README, it is sufficient to configure the plugin at the top-level `config.yml`.  For Spanner Wingnut, the feed will include full content of pages without limit on the number of posts in the feed.

{% codeblock "spanner/_config.yml" lang:yml https://github.com/orcmid/hexo-spanner "hexo-spanner" first_line:64 mark:65-70 %}
# RSS Feed                                                 # 0.0.10
feed:
  type: atom
  path: /hexo-atom.xml
  limit: 0
  hub:
  content: true
    
# Disqus (hat tip to John Stevenson)                        # 0.0.6
disqus_shortname: wingnut-1
  
# Home page setting
{% endcodeblock %}

## Result ##

The RSS button in the top right corner of the banner accesses the generated feed.

{% asset_image wingnut-RSS-atom.xml.png "generated Atom feed" %}

The feed format is acceptable to browsers and also feed readers, such as FeedDemon.

{% asset_image wingnut-FeedDemon-RSS-view.png "Typical FeedDemon presentation" %}

The exhibited excerpts are provided by the feed reader.  The expanded view is available directly without having to go to the Internet for the actual post.

## Observations

 * The Atom XML stream provides great detail.  
 
   * Updated dates are reported
 
   * Updates to older posts are reflected in the latest stream
 
   * Metadata includes information about categories and tags used on the post
 
 * The content of the post is in a CDATA block.  Styling information is not perpetuated, so highlighting in code blocks is not available and blockquote styling will be the default behavior of the feed reader.
 
 * Images, including screen captures, are perpetuated properly.  This is an alternative where code blocks do not provide what is desired in the RSS.  Fancybox viewing is not available, however.
 
 * Gallery posts lose the gallery in the RSS.  
 
 * Pull quotes appear as if they are simply preceding block quotes.  
 
 * no-title and link-title conditions of the original post are not perpetuated.  The RSS feed title links to the actual post, and a title is fabricated from a blog-text heading if necessary.
 
 * Previous unit test posts are now updated to reflect limitations that apply to RSS of the subject features.
 


