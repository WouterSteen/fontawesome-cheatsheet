---
layout: page
permalink: /font-awesome-react/
title: Font awesome React Usage 
description: Use font awesome with React
keywords: Font awesome react
---

### How to use font awesome with react

When you use a framework like react and you need some icons its a good idea to use font awesome. Why you would want that you can read on this page about <a href="/icon-fonts" title="The why and how about icon fonts">icon fonts</a> 
In general this is possible in two ways:

- Add the css and start working with it.

`https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.css`

Or - 
- use react-fontawesome

This is a great way to leverage fontawesome without the disadvantage of a icon font. This is that you load a font with icons you do not always use.
With react-fontawesome you compile the font with webpack, and not used icons are not in the bundle so no performance loss and good for the carbon footprint ;).
The fastest way to work with this is the method called explicit import of icons. 

Imagine you have a react app and need an icon:

```jsx

import ReactDOM from 'react-dom'
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome'
import { faTable } from '@fortawesome/free-solid-svg-icons'

const cheatSheetElement = <FontAwesomeCheatsheet icon={faTable} />

ReactDOM.render(cheatSheetElement, document.body)

```

Here you only bundle the table icon from the whole set of icons.

If you are planning to use more icons, its also possible to create a icon Library. This is a good idea when you use the same icon throughout you're entire app.
For this you need to the js file where you're app is initialized, lets say this file is called `fontawesomeCheatsheet.js`.

```jsx
import ReactDOM from 'react-dom'
import { library } from '@fortawesome/fontawesome-svg-core'
import { fab } from '@fortawesome/free-brands-svg-icons'
import { faCheckSquare, faTable } from '@fortawesome/free-solid-svg-icons'

library.add(fab, faCheckSquare, faTable)

```
In this file we import all brand icons, and the faCheckSquare and faTable icons. Then we do the magic, we import them into the library. In functional component files,
you can import `fortawesome/react-fontawesome` and use the icons that you just added. Like this:

```jsx

import React from 'react'
import { FontAwesomeIcon } from '@fortawesome/react-fontawesome'

export const Icon = () => (
  <div>
    <FontAwesomeIcon icon="check-square" />
    Favorite icon: <FontAwesomeIcon icon="table" />
  </div>
)

```

Notice that you do not use the `fa` prefix in functional components.

