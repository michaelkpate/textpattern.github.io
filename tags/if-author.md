---
layout: document
category: tags
published: true
title: "If author"
Description: The if_author tag will execute the contained statement if the called page is the result of an article search by a specific author's name.
tags:
  - Article tags
  - Conditional tags
---

# If author

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)
* [Genealogy](#genealogy)

## Syntax

~~~ html
<txp:if_author>
~~~

The **if_author** tag is a *conditional* tag and always used as an opening and closing pair, like this...

~~~ html
<txp:if_author>
    ...conditional statement...
</txp:if_author>
~~~

The tag will execute the contained statement **if** the called page is the result of an article search by a specific author's name.

Note: This is **not** the same as checking if the current article was written (posted) by the given author. Use [if_article_author](if-article-author) for that situation.
{: .alert-block .information}

## Attributes

Tag will accept the following attributes (**case-sensitive**):

`name="author"`
: Comma-separated list of author names.
: Default: unset, which determines whether 'any' author listing is being viewed.

`type="context"`
: Textpattern context to check against. You can choose from the following contexts (set to empty to include all contexts): \\
`article` is this an article author list? \\
`image` is this an image author list? \\
`file` is this a file author list? \\
`link` is this a link author list?
: Default: `article`.

## Examples

### Example 1: Select a stylesheet based on author

Selects a stylesheet named `author_list` when a list by author `admi` is being displayed, or a stylesheet determined by the active section for normal page display.

~~~ html
<txp:if_author name="admin">
    <link rel="stylesheet" href="<txp:css name="author_list" />" media="screen">
<txp:else />
    <link rel="stylesheet" href="<txp:css />" media="screen">
</txp:if_author>
~~~

Other tags used: [else](else), [css](css).

## Genealogy

### Version 4.3.0

`type` attribute added.
