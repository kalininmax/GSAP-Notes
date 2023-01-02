# Special Property: Stagger

The stagger property allows you to offset the start time of multiple targets in a single tween.

In GSAP3 you no longer need the staggerTo(), staggerFrom(), and staggerFromTo() methods of GSAP2.&#x20;

```javascript
// each image will start 0.2 seconds after the previous one starts.
gsap.to('#freds img', { y: -100, stagger: 0.2 });
```

A stagger object gives you greater control over where the staggers start from and how the timing is dispersed.

```javascript
gsap.to('#freds img', { y:-50, stagger: { each: 0.2, from: 'end' }});
```

&#x20;`each: 0.2` means there will be 0.2 seconds between the start of each animation.

&#x20;If instead you use `amount: 0.2` then all animations will start within 0.2 seconds.
