---
title: texture simple shapes
module: 9
jotted: false
---


# texture simple shapes

<div class="tab">
  <button class="tablinks active" onclick="openTab(event, 'Overview')">Overview</button>
  <button class="tablinks" onclick="openTab(event, 'example')">Example</button>  
  <button class="tablinks" onclick="openTab(event, 'todo')">To Do</button>  
</div>

<div id="Overview" class="tabcontent" style="display:block"  >
<div class="tabhtml" markdown="1">

### Overview

```js

let img;
function preload() {
  img = loadImage('assets/dog.jpg');
}

function setup() {
  createCanvas(100, 100, WEBGL);
}

function draw() {
  background(0);
  rotateZ(frameCount * 0.01);
  rotateX(frameCount * 0.01);
  rotateY(frameCount * 0.01);
  //pass image as texture
  texture(img);
  cylinder(20, 50);
}
```

```js

let img;
function preload() {
  img = loadImage('assets/dog.jpg');
}

function setup() {
  createCanvas(100, 100, WEBGL);
}

function draw() {
  background(0);
  rotateZ(frameCount * 0.01);
  rotateX(frameCount * 0.01);
  rotateY(frameCount * 0.01);
  //pass image as texture
  texture(img);
  cone(40, 70);
}
```

```js

let img;
function preload() {
  img = loadImage('assets/dog.jpg');
}

function setup() {
  createCanvas(100, 100, WEBGL);
}

function draw() {
  background(0);
  rotateZ(frameCount * 0.01);
  rotateX(frameCount * 0.01);
  rotateY(frameCount * 0.01);
  //pass image as texture
  texture(img);
   ellipsoid(30, 40, 40);
}
```

```js

let img;
function preload() {
  img = loadImage('assets/dog.jpg');
}

function setup() {
  createCanvas(100, 100, WEBGL);
}

function draw() {
  background(0);
  rotateZ(frameCount * 0.01);
  rotateX(frameCount * 0.01);
  rotateY(frameCount * 0.01);
  //pass image as texture
  texture(img);
  torus(30, 15);
}
```

</div>
</div>


<div id="todo" class="tabcontent">
<div class="tabhtml" markdown="1">
Try the code in the earlier tab to see the final result. Feel free to change values. 

<iframe src="https://editor.p5js.org/michaelcassens/sketches/4SYHBeKHm" width="100%" height="800px"></iframe>
</div>
</div>