---
layout: document
category: tags
published: true
title: "Comment anchor"
description: The comment_anchor tag is used to produce an empty anchor tag with an id attribute reflecting the comment ID.
tags:
  - Comment tags
---

# Comment anchor

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:comment_anchor />
~~~

The **comment_anchor** tag is a *single* tag which is used to produce an empty anchor tag with an id attribute reflecting the comment ID. Used in the form that renders your comments (the default form is named 'comments').

## Attributes

This tag has no attributes.

## Examples

### Example 1: Generate current comment anchor

~~~ html
<txp:comment_anchor />
<txp:comment_message />
~~~

When the comment number is `000005` you will see:

~~~ html
<a id="c000005"></a>
~~~

Other tags used: [comment_message](comment-message).
