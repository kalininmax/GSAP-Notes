# Timelines

A timeline is created with `gsap.timeline();`

All tweens in a timeline naturally play one after the other.

### Position Parameter

The position parameter allows you to offset the start time of tweens in a timeline:

```javascript
const tl = gsap.timeline();
  tl.to(object, { y: 300 }, '+=1')  // start 1 second after previous tween ends
  tl.to(object, { x: 300 }, '-=1')  // start 1 second before previous tween ends
  tl.to(object, { rotation: 90 }, '<')  // start when previous tween begins
  tl.to(object, { opacity: 0.5 }, '<1') // start 1 second after previous tween begins
  tl.to(object2, { x: 200 }, 1) // start exactly at a time of 1

```

Relative tweens using the "+=" and "-=" position parameters are placed relative to the end of the timeline, which isn't necessarily always the previous tween in the timeline.

### Timeline Control and Labels

Timelines have the exact same control methods as tween. Since you already know how to `play()` a tween you already know how to `play()` a timeline.

You must first create a reference to your timeline like:

```javascript
const animation = gsap.timeline()

// later on you can do
animation.play();
animation.pause();
animation.restart();
animation.reverse();
```

Labels allow you mark a specific point in time in your timeline.

You can add a label to a timeline using the `add()` method:

```javascript
const animation = gsap.timeline()
  .from('#demo', { duration: 1, opacity: 0 })
  .from('#title', { opacity: 0, duration: 3, scale: 0, ease: 'back' })
  .from('#freds img', { y: 160, stagger: 0.5, duration: 0.8, ease: 'back' }, '+=0.5')
  .add('test')
  .from('#time', { xPercent:100, duration:1, ease: 'bounce' });

animation.play('test');
```

**Links and More**

* [gsap.timeline() docs](https://greensock.com/docs/v3/GSAP/Timeline)
