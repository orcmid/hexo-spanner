---
title: Hexo Unit Test - Tag Plugins
date: 2017-12-10 14:28:21
categories:
- [Authoring, Markdown]
- [Blog Development, Hexo, landscape theme]
- [Blog Development, Hexo, plugins]
- [blogs, Spanner Wingnut]
tags:
- Hexo
- Landscape Theme
- Markdown
- Observations
- TODOs
- tags
---

This is the tenth in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) `tag-plugins.md` Post of 2013-12-25.  

Tag plugins have nothing to do with "tags" on posts.  The term applies to plugins that are exercised in template processing, including particular Markdown "tags" that invoke plugin functions.  See [Hexo Docs](https://hexo.io/docs/tag-plugins.html) for more information.  These tests follow the illustrations there.

## Block Quote ##

### Normal blockquote ##

This is the default formatting when using the ">" line leaders to make a block quote/indentation.  This behavior was already customized as part of the [Wingnut Markdown/HTML Elements](http://orcmid.com/BlunderDome/wingnut/2017/11/29/Elements/) unit test.

```
> Praesent diam elit, interdum ut pulvinar placerat, imperdiet at magna.
```

yields

> Praesent diam elit, interdum ut pulvinar placerat, imperdiet at magna.

Specialized formatting is by using Octopress tag insertions instead of "` >`".

### Quote from a book ###

```
{% blockquote David Levithan, Wide Awake %}
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.
{% endblockquote %}
```

yields

{% blockquote David Levithan, Wide Awake %}
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.
{% endblockquote %}

### Quote from Twitter (or any URL) ###

```
{% blockquote @DevDocs https://twitter.com/devdocs/status/356095192085962752 %}
NEW: DevDocs now comes with syntax highlighting. http://devdocs.io
{% endblockquote %}
```

yields

{% blockquote @DevDocs https://twitter.com/devdocs/status/356095192085962752 %}
NEW: DevDocs now comes with syntax highlighting. http://devdocs.io
{% endblockquote %}

### Quote from an article on the web ###

```
{% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing %}
Every interaction is both precious and an opportunity to delight.
{% endblockquote %}
```

yields

{% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing %}
Every interaction is both precious and an opportunity to delight.
{% endblockquote %}

### The Pattern ###

The general pattern is complicated.  It appears to be something like

```
{% blockquote [author/source [url] [title] ] %}
body
{% end blockquote %}
```



## Code Block ##

The normal code block and code font tagging in Markdown is via the \` character.  These also offer annotations for other features as part of GitHub-compatible markdown.  This test demonstrates how much the tag-plugin and standard approaches match.

One difference is that the \`\`\` boundaries can enclose a codeblock, but nothing can enclose \`\`\`  boundaries.

The codeblock tag format is

```
{% codeblock [title] [lang:language] [url] [link text] [mark:[#[-#][,..]%}
```

The backtick format is

> \`\`\` [language] [title] [url] [link text] 
> code snippet
> \`\`\`


### Normal code block ###

```
{% codeblock %}
alert('Hello World!');
{% endcodeblock %}
```
yields a plain codeblock,

{% codeblock %}
alert('Hello World!');
{% endcodeblock %}




### With caption

```
{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}
```

yields

{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}

### With caption and URL

```
{% codeblock _.compact http://underscorejs.org/#compact Underscore.js %}
_.compact([0, 1, false, 2, ‘’, 3]);
=> [1, 2, 3]
{% endcodeblock %}
```

yields

{% codeblock _.compact http://underscorejs.org/#compact Underscore.js %}
_.compact([0, 1, false, 2, ‘’, 3]);
=> [1, 2, 3]
{% endcodeblock %}

### With marked lines

```
{% codeblock lang:js mark:1,7-8,10 %}
const http = require('http');

const hostname = '127.0.0.1';
const port = 1337;

http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello World\n');
}).listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
{% endcodeblock %}
```

should have lines 1,7-8,10 marked with a selection coloring, yielding

{% codeblock lang:js mark:1,7-8,10 %}
const http = require('http');

const hostname = '127.0.0.1';
const port = 1337;

http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.end('Hello World\n');
}).listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
{% endcodeblock %}

Note: This depends on the theme's style supporting `.highlight.line.marked`, with the selection or current line coloring used.

### Gist

```
{% gist 996818 %}
```

will yield a particular Gist item

{% gist 996818 %}

### jsFiddle

```
{% jsfiddle ccWP7 %}
```

yields a particular JSFiddle in-line editing window

{% jsfiddle ccWP7 %}

There is more information about these at https://hexo.io/docs/tag-plugins.html

## Pullquote

Pullquotes add the pull quote item as a block on the left or right of the following Mardown paragraph.

### Left

```
{% pullquote left %}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{% endpullquote %}
```

will apply on the top-left corner of the paragraph that follows.

{% pullquote left %}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{% endpullquote %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Maecenas tempus molestie arcu, et fringilla mauris placerat ac. Nullam luctus bibendum risus. Ut cursus sed ipsum feugiat egestas. Suspendisse elementum, velit eu consequat consequat, augue lorem dapibus libero, eget pulvinar dolor est sit amet nulla. Suspendisse a porta tortor, et posuere mi. Pellentesque ultricies, mi quis volutpat malesuada, erat felis vulputate nisl, ac congue ante tortor ut ante. Proin aliquam sem vel mauris tincidunt, eget scelerisque tortor euismod. Nulla tincidunt enim nec commodo dictum. Mauris id sapien et orci gravida luctus id ut dui. In vel vulputate odio. Duis vel turpis molestie, scelerisque enim eu, lobortis eros. Cras at ipsum gravida, sagittis ante vel, viverra tellus. Nunc mauris turpis, elementum ullamcorper nisl pretium, ultrices cursus justo. Mauris porttitor commodo eros, ac ornare orci interdum in. Cras fermentum cursus leo sed mattis. In dignissim lorem sem, sit amet elementum mauris venenatis ac.

### Right

```
{% pullquote right %}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{% endpullquote %}
```

will apply on the top-<strike>left</strike>right corner of the paragraph that follows. *touched-up 2017-12-12*

{% pullquote right %}
Lorem ipsum dolor sit amet, consectetur adipiscing elit.
{% endpullquote %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed ligula justo, lobortis sit amet semper vel, dignissim sit amet libero. Praesent ac tempus ligula. Maecenas at gravida odio. Etiam tristique volutpat lacus eu faucibus. Donec non tempus arcu. Phasellus adipiscing, mauris nec mollis egestas, ipsum nunc auctor velit, et rhoncus lorem ipsum at ante. Praesent et sem in velit volutpat auctor. Duis vel mauris nulla. Maecenas mattis interdum ante, quis sagittis nibh cursus et. Nulla facilisi. Morbi convallis gravida tortor, ut fermentum enim gravida et. Nunc vel dictum nisl, non ultrices libero. Proin vestibulum felis eget orci consectetur lobortis. Vestibulum augue nulla, iaculis vitae augue vehicula, dignissim ultrices libero. Sed imperdiet urna et quam ultrices tincidunt nec ac magna. Etiam vel pharetra elit.

## Observations ##

 * This is a reminder that I very much want a different highlighting choice.   The grey on black doesn't work.
 
 * There are more tag plugins that might be tested.  It is not clear why those are omitted from the Unit Tests.  There are further variations to confirm for some of the tags.  
 
 * Spin out more tests as needed for features and changes specific to Spanner Wingnut and the intended family of *nfoCentrale* blogs.
 
 * It would be useful to have a way to select different highlightings in code blocks within a single post.  Perhaps there are clues to be found digging into how highlight is integrated.
 
