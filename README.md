# A-Frame-Component-Postprocessing
<img src="img/screenshot.gif" title="Video screen capture" alt="Video screen capture" height="400">

### **Description / Rationale**
This is the A-Frame component for post-processing effects, which are based on the examples provided by Three.js and other sources (see Tech Stack section for more information). The component makes use of Effect Composer and lets compose effects in the same way as it is done in Three.js.


### **Instructions**
In order to use the component attach "lenticular-image" to a-entity. The component has the following attributes: 
* <b>img1: { type: "string", default: "" }</b> - URL to first image.
* <b>img2: { type: "string", default: "" }</b> - URL to second image.

The code below shows the sample implementation of the component:
```
<html lang="en">
<head>
    <title>A-Frame Component: Post-Processing</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0">
    <script src="https://aframe.io/releases/1.4.2/aframe.min.js"></script>
    <script src="https://cdn.jsdelivr.net/gh/akbartus/A-Frame-Component-Postprocessing/dist/post-processing.min.js"></script>
</head>
<body>
    <a-scene post-processing="effect: bloom" >
        <a-box position="-1 0.5 -3" rotation="0 45 0" color="#4CC3D9"></a-box>
        <a-sphere position="0 1.25 -5" radius="1.25" color="#EF2D5E"></a-sphere>
        <a-cylinder position="1 0.75 -3" radius="0.5" height="1.5" color="#FFC65D"></a-cylinder>
        <a-plane position="0 0 -4" rotation="-90 0 0" width="4" height="4" color="#7BC8A4"></a-plane>
        <a-entity light="type: directional; color: #fff;" position="1 1 1"></a-entity>
        <a-sky color="#000"></a-sky> 
    </a-scene>
</body>
</html>
```

### **Updates**
Please note that the work on this component is still in progress. Future update will include:
* Possibility of adding custom effects.
* New effects.

### **Tech Stack**
The project is powered by AFrame and Three.js. The effects and corresponding examples were adapted from corresponding examples as provided in Three.js library as well as other sources (see: https://threejs.org/examples/?q=postprocessing, https://tympanus.net/codrops/2022/11/29/sketchy-pencil-effect-with-three-js-post-processing/, https://github.com/abberg/three-volumetric-light, https://github.com/felixturner/bad-tv-shader),  
        
### **Demo**
See demo of the component here: [Demo](https://lenticular-image.glitch.me/)
