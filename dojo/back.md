# Module: dojo/back

## Summary

Browser history management resources
## Methods

### _iframeLoaded
private method. Do not call this directly.

### addToHistory
adds a state object (args) to the history list.

### getHash


### goBack
private method. Do not call this directly.

### goForward
private method. Do not call this directly.

### init
Initializes the undo stack. This must be called from a <script>
block that lives inside the `<body>` tag to prevent bugs on IE.

Only call this method before the page's DOM is finished loading. Otherwise
it will not work. Be careful with xdomain loading or djConfig.debugAtAllCosts scenarios,
in order for this method to work, dojo/back will need to be part of a build layer.

### setHash


### setInitialState
Sets the state object and back callback for the very first page
that is loaded.

It is recommended that you call this method as part of an event
listener that is registered via dojo/ready.

# Constructor

## Methods

### hasOwnProperty


### toString


