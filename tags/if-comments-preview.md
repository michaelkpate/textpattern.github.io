---
layout: document
category: tags
published: true
title: "If comments preview"
Description: The if_comments_preview tag will execute the contained statements if a comment is being previewed.
tags:
  - Comment tags
  - Conditional tags
---

# If comments preview

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:if_comments_preview>
~~~

The **if_comments_preview** tag is a *conditional* tag and always used as an opening and closing pair, like this...

~~~ html
<txp:if_comments_preview>
    ...conditional statement...
</txp:if_comments_preview>
~~~

The tag will execute the contained statements if a comment is being previewed.

## Attributes

This tag takes no attributes:

## Examples

### Example 1: Display text prompt when comment is previewed

~~~ html
<txp:if_comments_preview>
    <p>
        <strong>Please review your comment before submitting.</strong>
    </p>
</txp:if_comments_preview>
