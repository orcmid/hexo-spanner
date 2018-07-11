---
title: Banner Bugfix Attempt 01
date: 2018-07-10 15:27:00
categories:
- [Blog Development, Hexo, landscape theme]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Banner
- Troubleshooting
- TODOs
- Internet Explorer
---
As remarked at [Returning to the Moon: Escape Tower Incident](https://orcmid.wordpress.com/2018/07/04/returning-to-the-moon-escape-tower-incident/), there is a problem with the rendering of the blog page header from the [Spanner Wingnut web-hosted blog](http://orcmid.com/BlunderDome/wingnut) when viewed by Internet Explorer.

{% asset_img wingnut-2018-07-04-1102-IEFailure.png "Corrupted IE11 Display" %}

This snuck through manual checking because I didn't confirm that there was any difference between browser viewing on my local machine and viewing on the hosted-site and its Apache HTTPD Server.

I am now working backwards to see if there were correct renderings of the page banner at any point in the past.

This post restores the original page-header banner image.

## Observations ##

 * This image renders correctly in both Edge and IE 11 at the [demonstration site](https://hexo.io/hexo-theme-landscape/) for the Hexo landscape theme.  I have restored the parameters and folder content.

 * Here is that image presented directly as an asset of this page, not as part of the page heading banner.  I don't usually employ JPEG images, and this is to verify that is not the problem.

{% asset_img banner.jpg "The image used in the banner styling" }

## To Dos ##

 * Update the Wingnut site to ensure that the new styles and banner immage asset are properly updated to the wingnut losted locations.

 * The RSS icon disappears on the corrupted presentation.  See about that if the problem persists.
