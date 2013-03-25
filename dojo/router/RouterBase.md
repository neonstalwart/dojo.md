# dojo/router/RouterBase

*Constructor*

## Summary

A module that allows one to easily map hash-based structures into
callbacks. The router module is a singleton, offering one central
point for all registrations of this type.
## Static Properties

### _currentPath


### _routeIndex


### _routes


### _started


### globMatch


### globReplacement


### idMatch


### idReplacement


## Static Methods

### _convertRouteToRegExp


### _getParameterNames


### _handlePathChange


### _indexRoutes


### _registerRoute


### go
A simple pass-through to make changing the hash easy,
without having to require dojo/hash directly. It also
synchronously fires off any routes that match.

### register
Registers a route to a handling callback

### registerBefore
Registers a route to a handling callback, except before
any previously registered callbacks

### startup
This method must be called to activate the router. Until
startup is called, no hash changes will trigger route
callbacks.
