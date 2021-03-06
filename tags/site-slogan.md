---
layout: document
category: tags
published: true
title: "Site slogan"
tags:
  - Markup tags
---

# Site slogan

On this page:

* [Syntax](#syntax)
* [Attributes](#attributes)
* [Examples](#examples)

## Syntax

~~~ html
<txp:site_slogan />
~~~

The **site_slogan** is a *single* tag which is used to output the site's tagline (labeled as 'Site slogan' in the [Preferences administration panel](../administration/preferences-panel)).

The slogan is a brief (255 characters maximum) tagline or description of your site which can be used, for example, in XML feeds.

## Attributes

This tag has no attributes.

## Examples

### Example 1: General display of slogan

~~~ html
<h2>
    <txp:site_slogan />
</h2>
~~~

### Example 2: Slogan as content filler

The slogan could be used for the content attribute of the `description` metadata element. Either whole...

~~~ html
<meta name="description" content="<txp:site_slogan />">
~~~

or partial...

~~~ html
<meta name="description" content="<txp:site_slogan />. And the rest of your pithy description would go here.">
