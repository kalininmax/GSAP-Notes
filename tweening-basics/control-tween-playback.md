# Control Tween Playback

Tween’s have a number of methods for controlling playback.

&#x20;In order to control a tween you need have way to reference it. Below we set up a variable to reference our tween.&#x20;

```javascript
const tween = gsap.to('#fred', { x: 600 });
```

To prevent a tween from playing automatically you can set its `paused` special property to `true`.

```javascript
const tween = gsap.to('#fred', { x: 600, paused: true });
```

To play that tween you can later call:&#x20;

```javascript
tween.play();
```
