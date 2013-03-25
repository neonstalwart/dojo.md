# Module: dojo/fx/easing

## Summary

Collection of easing functions to use beyond the default
`dojo._defaultEasing` function.
## Description

Easing functions are used to manipulate the iteration through
an `dojo.Animation`s _Line. _Line being the properties of an Animation,
and the easing function progresses through that Line determining
how quickly (or slowly) it should go. Or more accurately: modify
the value of the _Line based on the percentage of animation completed.

All functions follow a simple naming convention of "ease type" + "when".
If the name of the function ends in Out, the easing described appears
towards the end of the animation. "In" means during the beginning,
and InOut means both ranges of the Animation will applied, both
beginning and end.

One does not call the easing function directly, it must be passed to
the `easing` property of an animation.
## Methods

### backIn
An easing function that starts away from the target,
and quickly accelerates towards the end value.

Use caution when the easing will cause values to become
negative as some properties cannot be set to negative values.

### backInOut
An easing function combining the effects of `backIn` and `backOut`

### backOut
An easing function that pops past the range briefly, and slowly comes back.

### bounceIn
An easing function that 'bounces' near the beginning of an Animation

### bounceInOut
An easing function that 'bounces' at the beginning and end of the Animation

### bounceOut
An easing function that 'bounces' near the end of an Animation

### circIn


### circInOut


### circOut


### cubicIn


### cubicInOut


### cubicOut


### elasticIn
An easing function the elastically snaps from the start value

### elasticInOut
An easing function that elasticly snaps around the value, near
the beginning and end of the Animation.

### elasticOut
An easing function that elasticly snaps around the target value,
near the end of the Animation

### expoIn


### expoInOut


### expoOut


### linear
A linear easing function

### quadIn


### quadInOut


### quadOut


### quartIn


### quartInOut


### quartOut


### quintIn


### quintInOut


### quintOut


### sineIn


### sineInOut


### sineOut


# Constructor

## Methods

### hasOwnProperty


