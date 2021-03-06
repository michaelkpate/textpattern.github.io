---
layout: document
category: tags
published: true
title: "If first link"
Description: The if_first_link tag will execute the contained statements if the displayed link is the first in the currently displayed link list.
tags:
  - Conditional tags
  - Link tags
  - Structural tags
---

# If first link

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)
* [Genealogy](#genealogy)

## Syntax

~~~ html
<txp:if_first_link>
~~~

The **if_first_link** tag is a *conditional* tag and always used as an opening and closing pair, like this...

~~~ html
<txp:if_first_link>
    ...conditional statement...
</txp:if_first_link>
~~~

The tag will execute the contained statements if the displayed link is the first in the currently displayed [linklist](linklist). The tag supports [else](else).

## Attributes

This tag has no attributes.

## Examples

### Example 1: Identify first link in an link list

[todo:pw]

Other tags used:

## Genealogy

### Version 4.6.0

Tag support added.
