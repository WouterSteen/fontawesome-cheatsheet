---
layout: page
permalink: /icon-font/
title: Icon Font
description: Download Icon fonts
keywords: icon fonts
---

# Icon Font

### What is an icon font?

An icon font is a font that contains images. Kinda like the font
`Symbols` in the good old MS Word. 
Not only it can contain symbols but also glyphs.

### Why do we need this?

One of the key features of an icon font is you can style icons the same way as
you can style random text. This feature makes it very popular with web developers.
Another feature is that the font is infinite scaleable because a font is vectorized.
So a font icon looks very neat, in a very small size, but also very big!
This also means that you dont have to worry about retina screens. This is a font,
so its a vector, so it just scales up to 2x or 3x and the icon looks just as good as on normal screens.

A font is basicly a sprite of images. So, we load up a big set of icons in just one http request.
This is a advantage, but also a minor disadvantage. Obviously we dont use all the icons on our website. So if we load a font like
font awesome, then we load a lot of unused icons.

### Why just not PNG for all icons?

Because png does not scale well on retina screens. We have to use far more data transfers to achieve the same image quality.

Its hard to manage a good png sprite.
