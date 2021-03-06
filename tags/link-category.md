---
layout: document
category: tags
published: true
title: "Link category"
description: The link-category tag is a single tag which returns the link category as text.
tags:
  - Link tags
---

# Link category

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:link_category />
~~~

The **link-category** tag is a *single* tag which returns the link category as text. This tag is used in a Textpattern 'link' type @@Form template@@ or inside the [linklist](linklist) container tag to return information about the current link in a list of links.

## Attributes

Tag will accept the following attributes (**case-sensitive**):

`title="boolean"`
: Whether to display the category name or its title.
: Values: `0` (name), or `1` (title).
: Default: `0`.

### Common presentational attributes

These attributes, which affect presentation, are shared by many tags. Note that default values can vary among tags.

`class="class name"`
: HTML `class` to apply to the `wraptag` attribute value.
: Default: unset (see @@class cross-reference@@).

`label="text"`
: Label prepended to item.
: Default: unset (but see @@label cross-reference@@ for exceptions).

`labeltag="element"`
: HTML element to wrap (markup) label, specified without brackets (e.g. `labeltag="h3"`).
: Default: unset.

`wraptag="element"`
: HTML tag to wrap around category text, specified without brackets (e.g. `wraptag="p"`).
: Default: unset.

## Examples

### Example 1: Display a link with class attribute

~~~ html
<a href="<txp:link_url />">
    <txp:link_name escape="html" />
</a> | <txp:link_category title="1" />
~~~

Other tags used: [link_url](link-url), [link_name](link_name).
