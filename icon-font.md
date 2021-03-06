---
layout: page
permalink: /icon-font/
title: Icon Font
description: What is an icon font and why would I use this?
keywords: what and why icon fonts
---

### What is an icon font?

An icon font is a font that contains images. Kinda like the font `Symbols` in the good old MS Word. Not only it can contain symbols but also glyphs. A <a href="https://en.wikipedia.org/wiki/Glyph" target="_blank" title="Wikipedia Link to Glyphs">glyph</a> is the variety of designs of a character.

### Why do we need an icon font?

One of the key features of an icon font is you can style icons the same way as
you can style random text. This feature makes it very popular with web developers.
Another feature is that the font is infinite scaleable because a font is vectorized.
So a font icon looks very neat, in a very small size, but also very big!
This also means that you dont have to worry about retina screens. This is a font,
so its a vector, so it just scales up to 2x or 3x and the icon looks just as good as on normal screens.

A font is basicly a sprite of images. So, we load up a big set of icons in just one http request.
This is a advantage, but also a minor disadvantage. Obviously we dont use all the icons on our website. So if we load a font like
font awesome, then we load a lot of unused icons.

Because all icons we use on the site are loaded from one request, we make certain that all icons showing in a consistent manner.

We have a lot of css transform options for a icon font symbols, but this is not specific for a icon font.

#### So to sum it all up:
- Style icons just like text
- Infinite scaleable
- One request to get them all
- Consistency
- CSS transform options

### Why just not PNG for all icons?

Because png does not scale well on retina screens. We have to use far more data transfers to achieve the same image quality. Its hard to manage a good png sprite.

