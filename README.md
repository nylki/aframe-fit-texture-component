## aframe-fit-texture-component

A fit-texture component for [A-Frame](https://aframe.io) VR. The `fit-texure` component can be used with entities that use the `material` component with a image as texture. (Videos textures don't work yet).
Instead of modifying the texture, this component modifies the entities `geometry` (width/height) to match the textures dimensions perfectly.

![screenshot](https://cloud.githubusercontent.com/assets/1710598/14921020/431f7b42-0e30-11e6-9fdf-83f748ad3c2b.png)

### Usage

#### Browser Installation

Install and use by directly including the [browser files](dist):

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.2.0/aframe.min.js"></script>
  <script src="https://github.com/nylki/aframe-fit-texture-component/raw/master/dist/aframe-fit-texture-component.min.js"></script>
</head>

<body>
  <a-scene>
    <!--
    Before: This entity will have a stretched image,
    unless you know and specify width/height manually.
    -->
    <a-entity material="src: url(randomimage.png)">
    
    <!-- Now: The entity will scale according to the texture. -->
    <a-entity material="src: url(randomimage.png)" fit-texture>
      
    <!--using a fixed width works fine too, the height gets set automatically.-->
    <a-entity geometry="primitive: plane; width:21" material="src: url(randomimage.png)" fit-texture>
      
    <!--Same as above but with a fixed height:-->
    <a-entity geometry="primitive: plane; height:0.123" material="src: url(randomimage.png)" fit-texture>
      
    <!--`a-images` work of course:-->
    <a-image src="randomimage.jpg" fit-texure scale="2.0">

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
