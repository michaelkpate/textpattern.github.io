---
layout: document
category: tags
published: true
title: "Category2"
description: The category2 tag will display information of the category as defined by 'Category 2' of the article being displayed.
tags:
  - Article tags
  - Navigation tags
---

# Category2

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)
* [Genealogy](#genealogy)

## Syntax

~~~ html
<txp:category2 />
~~~

The **category2** tag can be used as either a *single* tag or *container* tag. It will display information of the category as defined by **Category 2** of the article being displayed. When used as a containing tag, it will turn the contents into a link to that category. Otherwise, it will return plain text.

This tag may be used within either an article form, or in a page, wrapped in an [if_individual_article](if-individual-article) conditional tag.

## Attributes

Tag will accept the following attributes (**case-sensitive**):

`link="boolean"`
: Whether to link to articles from the same category. Works only in the *single* tag.
: Values: `0` (no) or `1` (yes).
: Default: `0`.

`section="section name"`
: Restrict to articles from specified section(s).
: Values: (comma separated list of) section name(s).
: Default: unset, retrieves from all sections.

`title="boolean"`
: Whether to output category title, rather than name.
: Values: `0` (no, use name) or `1` (yes, use title).
: Default: `0`.

`this_section="boolean"`
: Whether to only link to articles from the section containing the current article.
: Values: `0` (no, allow from any section) or `1` (yes).
: Default: `0`.

### Common presentational attributes

These attributes, which affect presentation, are shared by many tags. Note that default values can vary among tags.

`class="class name"`
: HTML `class attribute` to be applied to `wraptag`.
: Default: unset (see @@class cross-reference@@).

`wraptag="tag"`
: HTML tag to wrap around output, specified without brackets (e.g. `wraptag="p"`).
: Default: unset (but see @@wraptag cross-reference@@ for exceptions).

## Examples

### Example 1: Category name in plain text

~~~ html
<p>
    <txp:category2 />
</p>
~~~

### Example 2: Hyperlinked category title

~~~ html
<p>
    <txp:category2 link="1" title="1" />
</p>
~~~

If **category2** is 'Specific stuff', this tag will display the words 'Specific stuff' as a hyperlink to a list of articles in the same category.

### Example 3: Container example

~~~ html
<p>
    <txp:category2>Other articles in category:
    <txp:category2 title="1" /></txp:category2>
</p>
~~~

### Example 4: Category 1 and 2

~~~ html
<p>
    Filed in: <txp:category1 link="1" title="1" />
    <txp:if_article_category number="2">
        and <txp:category2 link="1" title="1" />
    </txp:if_article_category>
</p>
~~~

Shows a hyperlinked category 1, and also hyperlinked category 2 but only if it is used.

Other tags used: [category1](category1), [if_article_category](if-article-category).

## Genealogy

### Version 4.0.4

`class`, `section`, `this_section` and `wraptag` attributes added.
