# Basic Tween

The basic syntax for a `gsap.to()` tween is as follows:

```javascript
// animates the element with a class of “fred” to an x position of 400
gsap.to('.fred', { x: 400 });
```

If you do not specify a duration, gsap will use the default which is 0.5 seconds (500ms).

You can change the default duration using:

```javascript
gsap.defaults({ duration: 1 });
```

Behind the scenes gsap changes the target’s inline style during the animation.

For best performance animate CSS Transform values and opacity:

* x and y
* rotation, rotationX, rotationY
* skewX and skewY
* scaleX, scaleY, or just scale &#x20;

GSAP can animate any numeric property you throw at it.

* width and height
* backgroundColor
* color
* padding
* left and top (must set position to relative, absolute, or fixed)
* vh and vw&#x20;

Changing values that are not CSS Transforms or opacity can cause the browser to re-do its layout of the page which in extreme situations can hinder performance. For a few tweens, it’s not the end of the world as some purists make it out to be.

**Links and More**

* [gsap.to() docs](https://greensock.com/docs/v3/GSAP/gsap.to\(\))
* [gsap.defaults() docs](https://greensock.com/docs/v3/GSAP/gsap.defaults\(\))
