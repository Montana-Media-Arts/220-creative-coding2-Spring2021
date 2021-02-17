---
title: Particle Class
module: 7
jotted: false
---


# Particle Class

What does the code look like?

```js
// Daniel Shiffman
// http://codingtra.in

// Simple Particle System
// https://youtu.be/UcdigVaIYAk

class Particle {

  constructor() {
    this.x = 300;
    this.y = 380;
    this.vx = random(-1, 1);
    this.vy = random(-5, -1);
    this.alpha = 255;
  }

  finished() {
    return this.alpha < 0;
  }

  update() {
    this.x += this.vx;
    this.y += this.vy;
    this.alpha -= 5;
  }

  show() {
    noStroke();
    //stroke(255);
    fill(255, this.alpha);
    ellipse(this.x, this.y, 16);
  }

}

```

Let's examine the class.

### Properties

There are five different properties.

```js
  this.x = 300;
  this.y = 380;
  this.vx = random(-1, 1);
  this.vy = random(-5, -1);
  this.alpha = 255;
```

We know that `x` and the `y` are the location of each of the particles.  What is the `vx` and `vy`?  That is the velocity of the x and y directions.  Finally, this particle system uses the `alpha` property to determine if the particle is alive or dead.

### Functions

In this class, there are three functions. It still functions like any other particle system with these functions. 

```js

 finished() {
    return this.alpha < 0;
  }

  update() {
    this.x += this.vx;
    this.y += this.vy;
    this.alpha -= 5;
  }

  show() {
    noStroke();
    //stroke(255);
    fill(255, this.alpha);
    ellipse(this.x, this.y, 16);
  }
```

So what do each of these functions do?

#### finished

```js
 finished() {
    return this.alpha < 0;
  }

```
This one is simple right?  This one just checks to see if the alpha value is less than zero and then let's the program know that the particle is dead.

#### update

```js

  update() {
    this.x += this.vx;
    this.y += this.vy;
    this.alpha -= 5;
  
```

This function is what makes the particles move.  So, it is adding the velocity of the particle to the x and y coordinates while decreasing the alpha property each frame.  As such, each particle moves and then the alpha decreases with each movement.

#### show

```js
  show() {
    noStroke();
    //stroke(255);
    fill(255, this.alpha);
    ellipse(this.x, this.y, 16);
  }
```

Finally, the show function displays the ellipse (this can be any other object, images, etc.) and uses the alpha to make it fade away. 