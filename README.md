## aframe-fit-texture-component

A fit-texture component for [A-Frame](https://aframe.io) VR. The `fit-texure` component can be used with entities that use the `material` component with a image as texture. (Videos textures don't work yet).
This component is intented for use with image planes, aka `a-image`.
However, feel free to experiment with others or create pull requests!

![screenshot](https://cloud.githubusercontent.com/assets/1710598/14921020/431f7b42-0e30-11e6-9fdf-83f748ad3c2b.png)

### Usage

#### Browser Installation

Install and use by directly including the [browser files](dist):

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.2.0/aframe.min.js"></script>
  <script src="https://rawgit.com/ngokevin/aframe-text-component/master/dist/aframe-text-component.min.js"></script>
</head>

<body>
  <a-scene>
    // before: This entity will have a stretched image, unless you know and specify width/height manually.
    <a-entity material="texture:randomimage.jpg">
    
    // now: The entity will scale according to the texture.
    <a-entity material="texture:randomimage.jpg" fit-texture>
    
  </a-scene>
</body>
```

#### NPM Installation

Install via NPM:

```bash
npm install aframe-fit-texture-component
```

Then register and use.

```js
require('aframe');
require('aframe-fit-texture-component');
```
