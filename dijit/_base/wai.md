# Module: dijit/_base/wai

## Summary

Deprecated methods for setting/getting wai roles and states.
New code should call setAttribute()/getAttribute() directly.

Also loads hccss to apply dj_a11y class to root node if machine is in high-contrast mode.
## Methods

### getWaiRole
Gets the role for an element (which should be a wai role).

### getWaiState
Gets the value of a state on an element.

### hasWaiRole
Determines if an element has a particular role.

### hasWaiState
Determines if an element has a given state.

### removeWaiRole
Removes the specified role from an element.
Removes role attribute if no specific role provided (for backwards compat.)

### removeWaiState
Removes a state from an element.

### setWaiRole
Sets the role on an element.

### setWaiState
Sets a state on an element.

