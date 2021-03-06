---
layout: document
category: tags
published: true
title: "Comments form"
Description: The comments_form tag is used to display a comment form.
tags:
  - Comment tags
---

# Comments form

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)
* [Genealogy](#genealogy)

## Syntax

~~~ html
<txp:comments_form />
~~~

The **comments_form** tag is a *single* tag which is used to display a comment form. Comments will be attached to present individual article as a default, or to the article set by the `id` attribute.

## Attributes

Tag will accept the following attributes (**case-sensitive**):

`form="form name"`
: Use specified form template.
: Default: `comment_form`.

### Common presentational attributes

These attributes, which affect presentation, are shared by many tags. Note that default values can vary among tags.

`class="CSS class name"`
: HTML `class` to apply to the `wraptag` attribute value.
: Default: `comments_form` (see @@class cross-reference@@).

`wraptag="tag"`
: HTML tag to wrap around output, specified without brackets (e.g. `wraptag="p"`).
: Default: unset (but see @@wraptag cross-reference@@ for exceptions).

## Examples

### Example 1: Give visitors indication of 'Comments' status

Comments for articles can be turned on or off at the author's discretion for any article that is published; by using the following scheme in an article form, you can still have the on/off control over comments while still giving users indication of comment status:

~~~ html
<txp:if_comments_allowed>
    <txp:comments_form />
<txp:else />
    <p>Comments are turned off for this article.</p>
</txp:if_comments_allowed>
~~~

Other tags used: [if_comments_allowed](if-comments-allowed), [else](else).

### Example 2: Display conditional comments and form

~~~ html
<txp:if_comments_allowed>
    <txp:comments form="lineitem" break="li" wraptag="ul" />
    <txp:comments_form />
</txp:if_comments_allowed>
~~~

And then an example of what the form `lineitem` could contain:

~~~ html
<txp:comment_id />
~~~

For the current article, returns a list of id numbers for comments and a comment input form (but only if comments are currently allowed).

Other tags used: [comment_id](comment-id), [comments](comments), [if_comments_allowed](if-comments-allowed).

## Genealogy

### Version 4.6.0

`msgstyle` attribute deprecated. \\
`forgetlabel`, `isize`, `msgcols`, `msgrows`, `msgstyle`, `previewlabel`, `rememberlabel` and `submitlabel` attributes deprecated and functionality moved to individual `comment_*` input tags.

### Version 4.5.0

Added `forgetlabel`, `previewlabel`, `rememberlabel` and `submitlabel` attributes.

### Version 4.0.4

`show_preview` attribute removed.
