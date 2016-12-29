react-scrollable-anchor
=====================

[![npm version](https://img.shields.io/npm/v/react-scrollable-anchor.svg?style=flat-square)](https://www.npmjs.com/package/react-scrollable-anchor)

Lightweight and dynamic anchors in React.

```js
npm install --save react-scrollable-anchor
```

## Usage

### 1. Creating a scrollable anchor

Use the `ScrollableAnchor` tag to wrap any React element, making it a scrollable anchor.

```js
import React, { Component } from 'react'
import ScrollableAnchor from 'react-scrollable-anchor'

export default class Page extends Component {
  render() {
    return (
      <div style={styles.container}>
        <ScrollableAnchor id={'section1'}>
          <div>
            <span> Hello World </span>
          </div>
        </ScrollableAnchor>
        <ScrollableAnchor id={'section2'}>
          <div>
            <span> How are you world? </span>
          </div>
        </ScrollableAnchor>
      </div>
    )
  }
}
```

### 2. Configure

Access configureAnchors to customize scrolling and anchors.

##### Offset all scrollable anchors by a fixed amount

```js
import { configureAnchors } from 'react-scrollable-anchor'

// Offset all anchors by -60 to account for a fixed header
// and scroll more quickly than the default 400ms
configureAnchors({offset: -60, scrollDuration: 200})
```

##### Options:

----------------   ----------------
option             default
----------------   ----------------
`offset`           `0`
`scrollDuration`   `false`
----------------   ----------------

### 3. Utilities

A small toolkit of scrolling utilies for use with anchors

##### Jump to top of page in a way that plays nicely with scrollable anchors

```js
import { goToTop } from 'react-scrollable-anchor'

// scroll to top of the page
goToTop()
```

##### Scroll to any scrollable anchor, with option to record history

```js
import { goToAnchor } from 'react-scrollable-anchor'

// scroll to #section1 without saving that hash update in history
goToAnchor('section1')
goToAnchor('section1', false)

// scroll to #section1, saving that hash update in history
goToAnchor('section1', true)
```

## Issues and feature requests

Please open issues on Github. Issues are easier to address if you include
context and code samples.

## Contributing

Please contribute!

## Feedback or contact

Feel free to contact me at gabergg@gmail.com.
