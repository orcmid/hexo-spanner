---
title: Hexo Unit Test - Wingnut Markdown/HTML Elements
date: 2017-11-29 16:12:39
updated: 2017-12-03 16:15:00
categories:
 - [Blog Development, Hexo, landscape theme]
 - [blogs, Spanner Wingnut]
 - [Authoring, Markdown, HTML]
tags:
 - Hexo 
 - Landscape Theme
 - Markdown
 - Text Elements
 - TODOs
 - Observations
---

This is the second in a series of Spanner Wingnut confirmation tests using the Hexo Unit Tests for Themes.  This test demonstrates basic support for Markdown elements and direct HTML elements in the Markdown.

The test is derived from the [hexo-theme-unit-test](https://github.com/hexojs/hexo-theme-unit-test) "Elements" test post of 2013-12-24.

## Heading Check ##

This test reveals the formatting that is currently created for six levels of MarkDown/HTML headings.

The MarkDown source is simply
```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

Here are the formatted results

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

## Paragraph Formatting ##

These paragraphs include a variety of in-line formatting styles.  To make comparison easier, the original MarkDown is broken into separate lines.

### First Paragraph ###

#### 1st Paragraph MarkDown Source ####

```
Lorem ipsum dolor sit amet, [test link]() consectetur adipiscing elit. 
**Strong text** pellentesque ligula commodo viverra vehicula. *Italic text* 
at ullamcorper enim. Morbi a euismod nibh. <u>Underline text</u> non elit nisl.
~~Deleted text~~ tristique, sem id condimentum tempus, metus lectus venenatis
mauris, sit amet semper lorem felis a eros. Fusce egestas nibh at sagittis 
auctor. Sed ultricies ac arcu quis molestie. Donec dapibus nunc in nibh 
egestas, vitae volutpat sem iaculis. Curabitur sem tellus, elementum nec quam
id, fermentum laoreet mi. Ut mollis ullamcorper turpis, vitae facilisis velit
ultricies sit amet. Etiam laoreet dui odio, id tempus justo tincidunt id.
Phasellus scelerisque nunc sed nunc ultricies accumsan.
```

#### 1st Paragraph Generated Text ####

Lorem ipsum dolor sit amet, [test link]() consectetur adipiscing elit.  **Strong text** pellentesque ligula commodo viverra vehicula. *Italic text* at ullamcorper enim. Morbi a euismod nibh. <u>Underline text</u> non elit nisl. ~~Deleted text~~ tristique, sem id condimentum tempus, metus lectus venenatis mauris, sit amet semper lorem felis a eros. Fusce egestas nibh at sagittis auctor. Sed ultricies ac arcu quis molestie. Donec dapibus nunc in nibh egestas, vitae volutpat sem iaculis. Curabitur sem tellus, elementum nec quam id, fermentum laoreet mi. Ut mollis ullamcorper turpis, vitae facilisis velit ultricies sit amet. Etiam laoreet dui odio, id tempus justo tincidunt id. Phasellus scelerisque nunc sed nunc ultricies accumsan.

### Second Paragraph ###

#### 2nd Paragraph MarkDown Source ####

```
Interdum et malesuada fames ac ante ipsum primis in faucibus. `Sed erat diam`,
blandit eget felis aliquam, rhoncus varius urna. Donec tellus sapien, sodales 
eget ante vitae, feugiat ullamcorper urna. Praesent auctor dui vitae dapibus 
eleifend. Proin viverra mollis neque, ut ullamcorper elit posuere eget.
```

#### 2nd Paragraph Generated Text ####

Interdum et malesuada fames ac ante ipsum primis in faucibus. `Sed erat diam`, blandit eget felis aliquam, rhoncus varius urna. Donec tellus sapien, sodales eget ante vitae, feugiat ullamcorper urna. Praesent auctor dui vitae dapibus eleifend. Proin viverra mollis neque, ut ullamcorper elit posuere eget.

### Third Paragraph - *updated 2017-12-01 for wingnut* ###

#### 3rd Paragraph Block Quote MarkDown Source ####

```
> Praesent diam elit, interdum ut pulvinar placerat, imperdiet at magna. 
*updated 2017-12-01* to appear as ordinary text indented.
> > *added 2017-12-01* to confirm additional indentation per level. 
```

#### 3rd Paragraph Generated Block Quote Text ####

> Praesent diam elit, interdum ut pulvinar placerat, imperdiet at magna.  *updated 2017-12-01* to appear as ordinary text indented.
> > *added 2017-12-01* to confirm additional indentation per level. 

## List Types ##

Various list types are tied to HTML elements for the same purposes.  There are more variations than those checked on here.  These are an essential minimum.

### Definition List (dl) ###

#### Definition List Source ####

This is a pure insertion of HTML elements

```
<dl><dt>Definition List Title</dt><dd>This is a definition list division.</dd></dl>
```

#### Definition List Generation ####

<dl><dt>Definition List Title</dt><dd>This is a definition list division.</dd></dl>

### Ordered List (ol) ###

#### Ordered List Markdwon ####

```
1. List Item 1
2. List Item 2
3. List Item 3
```

#### Ordered List Generation ####

1. List Item 1
2. List Item 2
3. List Item 3

### Unordered List (ul) ###

#### Unordered List Markdown Source ####

```
- List Item 1
- List Item 2
- List Item 3
```

#### Unordered List Generation ####

- List Item 1
- List Item 2
- List Item 3

## Table ##

There is more variation to be considered in the use of tables.  Here is a fundamental test.

### Table Markdown Source ###

```
| Table Header 1 | Table Header 2 | Table Header 3 |
| - | - | - |
| Division 1 | Division 2 | Division 3 |
| Division 1 | Division 2 | Division 3 |
| Division 1 | Division 2 | Division 3 |
```

### Generated Table ###

| Table Header 1 | Table Header 2 | Table Header 3 |
| - | - | - |
| Division 1 | Division 2 | Division 3 |
| Division 1 | Division 2 | Division 3 |
| Division 1 | Division 2 | Division 3 |

## Misc Stuff - abbr, acronym, sub, sup, etc. ##

### Miscellaneous MarkDown Usage ###

These are all via HTML elements.  Superscripts and Subscripts should be apparent.  Some other elements might not have visible indicators except for the possibility of mouse-over indications.

### MarkDown Text ###

```
Lorem <sup>superscript</sup> dolor <sub>subscript</sub> amet, consectetuer
adipiscing elit. Nullam dignissim convallis est. Quisque aliquam.
<cite>cite</cite>. Nunc iaculis suscipit dui. Nam sit amet sem. Aliquam libero
nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. Praesent mattis,
massa quis luctus fermentum, turpis mi volutpat justo, eu volutpat enim diam
eget metus. Maecenas ornare tortor. Donec sed tellus eget sapien fringilla
nonummy. <acronym title="National Basketball Association">NBA</acronym> Mauris
a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc.
Morbi imperdiet augue quis tellus.  <abbr title="Avenue">AVE</abbr>
```

### Generated Text ###

Lorem <sup>superscript</sup> dolor <sub>subscript</sub> amet, consectetuer adipiscing elit. Nullam dignissim convallis est. Quisque aliquam. <cite>cite</cite>. Nunc iaculis suscipit dui. Nam sit amet sem. Aliquam libero nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. Praesent mattis, massa quis luctus fermentum, turpis mi volutpat justo, eu volutpat enim diam eget metus. Maecenas ornare tortor. Donec sed tellus eget sapien fringilla nonummy. <acronym title="National Basketball Association">NBA</acronym> Mauris a ante. Suspendisse quam sem, consequat at, commodo vitae, feugiat in, nunc. Morbi imperdiet augue quis tellus.  <abbr title="Avenue">AVE</abbr>

## Observations

 * Assuming that these tests all render appropriately, the styling will be adjusted to have them also be pleasant for Spanner Wingnut's Muddleware Lab, and its sibling blogs.
 
  * Definition lists should have the details indented beneath the title.
  
  * Tables are all right.  Other variants are desirable.  These must be found.
  
> *updated 2017-12-03* Adding observations and adjusting categories/tags
