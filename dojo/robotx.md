# Module: dojo/robotx

## Properties

### doc


### mouseWheelSize


### window


## Methods

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

