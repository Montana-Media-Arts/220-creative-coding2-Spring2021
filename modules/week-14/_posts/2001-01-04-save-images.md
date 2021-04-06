---
title: Create Movie
module: 14
jotted: true
---

# Create a Movie

Using p5, we can also create movies by autogenerating several frames and then stitching them together.

Here is an example of auto-generating squares.

```js
var mainColor = 255;

function setup() {
    createCanvas(640, 480);
    background(0);
    frameRate(25);
    noStroke();
    rectMode(CENTER);
}
function draw() {
    fill(mainColor,mainColor,mainColor, random(100));

    var size= random(200);

    rect(random(width), random(height), size, size);

    if (frameCount % 200 == 0) {
        mainColor = 255 - mainColor; // 255 0 255 0 255 0 ..
    }
    saveFrames("myMovie",".png",1,25);

    if (frameCount > 25) { // 1 second * 25 fps = 25
        noLoop();
    }
}
```

There's a lot here as well.  How does it work?

```js
  createCanvas(640, 480);
  background(0);
  frameRate(25);
  noStroke();
  rectMode(CENTER);
```

Then,...

```js
    fill(mainColor,mainColor,mainColor, random(100));

    var size= random(200);

    square(random(width), random(height), size);

    if (frameCount % 5 == 0) {
        mainColor = 255 - mainColor; // 255 0 255 0 255 0 ..
    }
    saveFrames("myMovie",".png",1,25);

    if (frameCount > 25) { // 1 second * 25 fps = 25
        noLoop();
    }
```

Then,...

```js
  if (frameCount % 5 == 0) {
      mainColor = 255 - mainColor; // 255 0 255 0 255 0 ..
  }
```

Then,...

```js
  saveFrames("myMovie",".png",1,25);
```

Finally, ...

```js
  if (frameCount > 25) { // 1 second * 25 fps = 25
      noLoop();
  }
```

Now, alter the example from above.

<iframe src="https://editor.p5js.org/" width="100%" height="800px"></iframe>