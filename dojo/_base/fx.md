# Module: dojo/_base/fx

## Summary

This module defines the base dojo/_base/fx implementation.
## Methods

### Animation
A generic animation class that fires callbacks into its handlers
object at various states.

### anim
A simpler interface to `animateProperty()`, also returns
an instance of `Animation` but begins the animation
immediately, unlike nearly every other Dojo animation API.

### animateProperty
Returns an animation that will transition the properties of
node defined in `args` depending how they are defined in
`args.properties`


### fadeIn
Returns an animation that will fade node defined in 'args' from
its current opacity to fully opaque.

### fadeOut
Returns an animation that will fade node defined in 'args'
from its current opacity to fully transparent.

