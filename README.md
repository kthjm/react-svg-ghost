# react-power-path

[![npm](https://img.shields.io/npm/v/react-power-path.svg?style=flat-square)](https://www.npmjs.com/package/react-power-path)
[![npm](https://img.shields.io/npm/dm/react-power-path.svg?style=flat-square)](https://www.npmjs.com/package/react-power-path)
[![Build Status](https://img.shields.io/travis/kthjm/react-power-path.svg?style=flat-square)](https://travis-ci.org/kthjm/react-power-path)
[![Coverage Status](https://img.shields.io/codecov/c/github/kthjm/react-power-path.svg?style=flat-square)](https://codecov.io/github/kthjm/react-power-path)
[![cdn](https://img.shields.io/badge/jsdelivr-latest-e84d3c.svg?style=flat-square)](https://cdn.jsdelivr.net/npm/react-power-path/dist/react-power-path.min.js)

enhanced `<path />` that recieve its totalLength via specific styles.

## Installation
```shell
yarn add react-power-path
```

## Usage
```js
import React from 'react'
import Path from 'react-power-path'

export default (props) => (
  <svg viewBox='0 0 300 300'>
    <g>
      <Path {...{
        d: 'M 100 100 L 300 100 L 200 300 z',
        style: {
          strokeDasharray: (totalLength) => {},
          strokeDashoffset: (totalLength) => {},
          animation: (totalLength) => {},
          animationName: (totalLength) => {},
        }
      }} />
    </g>
  </svg>
)

```

## API

specific styles:
- `strokeDasharray`
- `strokeDashoffset`
- `animation`
- `animationName`

If they are set as function, the totalLength passed, and the result will be value. Or set as values, nothing happens.

> `react-power-path` depend on [`createElementNS`](https://developer.mozilla.org/ja/docs/Web/API/Document/createElementNS) and [`path.getTotalLength`](https://developer.mozilla.org/en-US/docs/Web/API/SVGGeometryElement/getTotalLength).

## License
MIT (http://opensource.org/licenses/MIT)
