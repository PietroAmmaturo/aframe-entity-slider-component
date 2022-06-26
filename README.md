## aframe-slideshow-component

[![Version](http://img.shields.io/npm/v/aframe-slideshow-component.svg?style=flat-square)](https://npmjs.org/package/aframe-slideshow-component)
[![License](http://img.shields.io/npm/l/aframe-slideshow-component.svg?style=flat-square)](https://npmjs.org/package/aframe-slideshow-component)

Used to create a slideshow of aframe entities

For [A-Frame](https://aframe.io).

### API

| Property | Description | Default Value |
| duration | animation duration (in seconds) | 2 |
|offset|vector connecting previous element to next element|2 0 0|
|forwardTrigger|selector to the forward trigger|mandatory|
|backwardTrigger|selector to the forward trigger|mandatory|
|toShow|how many elements to show at once|4|

### Installation

#### Browser

Install and use by directly including the [browser files](dist):

### Usage

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/1.3.0/aframe.min.js"></script>
  <script src="https://unpkg.com/aframe-slideshow-component@1.0.0/dist/aframe-slideshow-component.min.js"></script>
</head>

<body>
  <a-scene>
    <a-entity id="slider" position="-3 2 -5" slideshow="backwardTrigger: #left; forwardTrigger: #right;">
      <!--slides-->
    </a-entity>
    <a-entity position="0 1 -1" scale="0.2 0.2 0.2">
      <!--triggers-->
      <a-cylinder class="clickable"  position="-2 0 0" color="cyan" segments-radial="3" rotation ="0 40 0" id="left"></a-cylinder>
      <a-cylinder class="clickable"  position="2 0 0" color="crimson" segments-radial="3" rotation ="0 -40 0" id="right"></a-cylinder>
    </a-entity>
  </a-scene>
</body>
```

#### npm

Install via npm:

```bash
npm install aframe-slideshow-component
```

Then require and use.

```js
require('aframe');
require('aframe-slideshow-component');
```
