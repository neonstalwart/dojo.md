# Module: dojo/robotx

## Properties

### _appletDead


### _loaded
Deferred that resolves when the _initRobot() has been called.
Note to be confused with dojo/robotx.js, which defines initRobot() without an underscore

### _primePump


### _robotInitialized


### _robotLoaded


### _runsemaphore


### _spaceReceived


### _started
Deferred that resolves when startRobot() has signaled completing by typing on the keyboard,
which in turn calls _run().

### doc


### mouseWheelSize


### window


## Methods

### _assertRobot


### _getWindowChain


### _initKeyboard


### _initRobot


### _initWheel


### _killApplet


### _mouseMove


### _notified


### _onKeyboard


### _position


### _resolveNode


### _run


### _scrollIntoView


### _setDocumentBounds


### _updateDocument
Called every time a new page is loaded into the iframe, to setup variables
Point dojo.global, dojo.publish, etc. to refer to iframe.
Remove for 2.0?

### initRobot
Opens the application at the specified URL for testing, redirecting dojo to point to the application
environment instead of the test environment.

### keyDown
Holds down a single key, like SHIFT or 'a'.

### keyPress
Types a key combination, like SHIFT-TAB.

### keyUp
Releases a single key, like SHIFT or 'a'.

### killRobot


### mouseClick
Convenience function to do a press/release.
See robot.mousePress for more info.

### mouseMove
Moves the mouse to the specified x,y offset relative to the viewport.

### mouseMoveAt
Moves the mouse over the specified node at the specified relative x,y offset.

### mouseMoveTo
Move the mouse from the current position to the specified point.
Delays reading contents point until queued command starts running.
See mouseMove() for details.

### mousePress
Presses mouse buttons.

### mouseRelease
Releases mouse buttons.

### mouseWheel
Spins the mouse wheel.

### scrollIntoView
Scroll the passed node into view, if it is not.

### sequence
Defer an action by adding it to the robot's incrementally delayed queue of actions to execute.

### setClipboard
Set clipboard content.

### startRobot


### typeKeys
Types a string of characters in order, or types a dojo.keys.* constant.

### waitForPageToLoad
Notifies DOH that the doh.robot is about to make a page change in the application it is driving,
returning a doh.Deferred object the user should return in their runTest function as part of a DOH test.

# Constructor

## Methods

### hasOwnProperty


### toString


