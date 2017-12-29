---
title: Hexo Landscape Theme LinkedIn Sharing
date: 2017-12-27 19:54:21
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
- LinkedIn
---
Migration to a new blogging platform, Hexo, is being worked out gradually.  Experimental customizations of Hexo-generated blogging is at the Spanner Wingnut Muddleware Lab.  Upon customization stability, other blogs are restored using simple variations. 

This is the fourteenth in a series of Spanner Wingnut unit-test confirmations.  This post confirms the sharing of posts to LinkedIn, expanding sharing facility that is installed by default.  

LinkedIn sharing is added to the "Share" options available at the bottom of every post.  The necessary modifications are from the [hexo-theme-landscape](https://github.com/hexojs/hexo-theme-landscape) [Pull Request #100](https://github.com/hexojs/hexo-theme-landscape/pull/100) by @[itsAmr](https://github.com/itsAmr). 

{% asset_img wingnut-2017-12-27-2003-LinkedInShare.png "Share options" %}

On selection, after any login-requirement, a form is offered for describing the shared post.

{% asset_img wingnut-2017-12-27-2115-LinkedInShare.png "LinkedIn Share Submission" %}

The submission becomes part of the sharing-user's LinkedIn activity stream, as on my profile page.

{% asset_img wingnut-2017-12-28-1934-LinkedInShare.png "Shared 'update' Activity addition" %}

The update entry provides the excerpt (when there is one) and the submitted "update" text, along with a link to the subject post.

{% asset_img wingnut-2017-12-28-1929-LinkedInShare.png "Update Text" %}

## Observations ##

 * The additional sharing will automatically appear on existing pages that have a share button, including fixed pages (such as About) along with existing posts.
 
 * The LinkedIn form does not always provide an automatically-derived excerpt.  It is unclear how that might be influenced by the author of the post.
  
