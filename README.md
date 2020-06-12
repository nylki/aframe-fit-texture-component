## aframe-fit-texture-component

A fit-texture component for [A-Frame](https://aframe.io) VR. The `fit-texture` component can be used with entities that use the `material` component with a image or video as texture.
Instead of modifying the texture, this component modifies the entities `geometry` (width/height) to match the textures dimensions perfectly. Tested in A-Frame 1.0.4.

[![screenshot](https://cloud.githubusercontent.com/assets/1710598/14921020/431f7b42-0e30-11e6-9fdf-83f748ad3c2b.png)](https://nylki.github.io/aframe-fit-texture-component/)


### Usage

#### Browser Installation

Install and use by directly including the [browser files](dist):

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
  <script src="https://unpkg.com/aframe-lsystem-component/dist/aframe-lsystem-component.min.js"></script>
  <!-- or better: download aframe and this component, and server it from your local directory -->
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
    <a-image src="randomimage.jpg" fit-texture scale="2.0">
      
    <!-- As well as `a-video` -->
    <a-video src="somevideofile.mp4" position="0 1.75 -1.999" fit-texture></a-video>

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
