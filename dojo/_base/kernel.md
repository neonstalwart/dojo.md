# dojo/_base/kernel

## Summary

This module is the foundational module of the dojo boot sequence; it defines the dojo object.
## Static Properties

### Stateful


### __IoArgs


### __IoCallbackArgs


### __IoPublish


### __XhrArgs


### _blockAsync


### _contentHandlers
A map of available XHR transport handle types. Name matches the
`handleAs` attribute passed to XHR calls.

### _defaultContext


### _hasResource


### _initFired


### _name


### _nodeDataCache


### _postLoad


### _windowUnloaders


### back
Browser history management resources

### baseUrl
The directory in which `dojo.js` is located. Under normal
conditions, Dojo auto-detects the correct location from which it
was loaded. You may need to manually configure `baseUrl` in cases
where you have renamed `dojo.js` or in which `<base>` tags confuse
some browsers (e.g. IE 6). The variable `dojo.baseUrl` is assigned
either the value of `djConfig.baseUrl` if one is provided or the
auto-detected root if not. Other modules are located relative to
this path. The path should end in a slash.

### behavior


### cldr


### colors


### config
This module defines the user configuration during bootstrap.

### connectPublisher
Ensure that every time obj.event() is called, a message is published
on the topic. Returns a handle which can be passed to
dojo.disconnect() to disable subsequent automatic publication on
the topic.

### contentHandlers
A map of available XHR transport handle types. Name matches the
`handleAs` attribute passed to XHR calls.

### currency
localized formatting and parsing routines for currencies

### data


### date


### dijit


### dnd


### doc
Alias for the current document. 'doc' can be modified
for temporary context shifting. See also withDoc().

### dojox


### fx
Effects library on top of Base animations

### gears
TODOC

### global
Alias for the current window. 'global' can be modified
for temporary context shifting. See also withGlobal().

### html
TODOC

### i18n
This module implements the dojo/i18n! plugin and the v1.6- i18n API

### io


### isAir
True if client is Adobe Air

### isAndroid
Version as a Number if client is android browser. undefined otherwise.

### isAsync


### isBrowser
True if the client is a web-browser

### isChrome
Version as a Number if client is Chrome browser. undefined otherwise.

### isFF
Version as a Number if client is FireFox. undefined otherwise. Corresponds to
major detected FireFox version (1.5, 2, 3, etc.)

### isIE
Version as a Number if client is MSIE(PC). undefined otherwise. Corresponds to
major detected IE version (6, 7, 8, etc.)

### isIos
Version as a Number if client is iPhone, iPod, or iPad. undefined otherwise.

### isKhtml
Version as a Number if client is a KHTML browser. undefined otherwise. Corresponds to major
detected version.

### isMac
True if the client runs on Mac

### isMoz
Version as a Number if client is a Mozilla-based browser (Firefox,
SeaMonkey). undefined otherwise. Corresponds to major detected version.

### isMozilla
Version as a Number if client is a Mozilla-based browser (Firefox,
SeaMonkey). undefined otherwise. Corresponds to major detected version.

### isOpera
Version as a Number if client is Opera. undefined otherwise. Corresponds to
major detected version.

### isQuirks
Page is in quirks mode.

### isSafari
Version as a Number if client is Safari or iPhone. undefined otherwise.

### isSpidermonkey


### isWebKit
Version as a Number if client is a WebKit-derived browser (Konqueror,
Safari, Chrome, etc.). undefined otherwise.

### isWii
True if client is Wii

### keys
Definitions for common key values.  Client code should test keyCode against these named constants,
as the actual codes can vary by browser.

### locale
The locale to assume for loading localized resources in this page,
specified according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt).
Must be specified entirely in lowercase, e.g. `en-us` and `zh-cn`.
See the documentation for `dojo.i18n` and `dojo.requireLocalization`
for details on loading localized resources. If no locale is specified,
Dojo assumes the locale of the user agent, according to `navigator.userLanguage`
or `navigator.language` properties.

### mouseButtons


### number
localized formatting and parsing routines for Number

### parser
The Dom/Widget parsing package

### publish
Invoke all listener method subscribed to topic.

### query


### regexp
Regular expressions and Builder resources

### rpc


### scopeMap


### store


### string
String utilities for Dojo

### subscribe
Attach a listener to a named topic. The listener function is invoked whenever the
named topic is published (see: dojo.publish).
Returns a handle which is needed to unsubscribe this listener.

### tests
D.O.H. Test files for Dojo unit testing.

### toJsonIndentStr


### touch
This module provides unified touch event handlers by exporting
press, move, release and cancel which can also run well on desktop.
Based on http://dvcs.w3.org/hg/webevents/raw-file/tip/touchevents.html
Also, if the dojoClick property is set to true on a DOM node, dojo/touch generates
click events immediately for this node and its descendants, to avoid the
delay before native browser click events, and regardless of whether evt.preventDefault()
was called in a touch.press event listener.


### version
Version number of the Dojo Toolkit

### window
TODOC

## Static Methods

### AdapterRegistry
A registry to make contextual calling/searching easier.

### Animation
A generic animation class that fires callbacks into its handlers
object at various states.

### Color
Takes a named string, hex string, array of rgb or rgba values,
an object with r, g, b, and a properties, or another `Color` object
and creates a new Color instance to work from.


### Deferred
Deprecated.   This module defines the legacy dojo/_base/Deferred API.
New code should use dojo/Deferred instead.

### DeferredList
Deprecated, use dojo/promise/all instead.
Provides event handling for a group of Deferred objects.

### NodeList
Array-like object which adds syntactic
sugar for chaining, common iteration operations, animation, and
node manipulation. NodeLists are most often returned as the
result of dojo.query() calls.

### _Animation
A generic animation class that fires callbacks into its handlers
object at various states.

### _Line
Object used to generate values from a start value to an end value

### _Url


### __toPixelValue
converts style value to pixels on IE or return a numeric value.

### _defaultEasing
The default easing function for Animation(s)

### _destroyElement


### _docScroll
Returns an object with {node, x, y} with corresponding offsets.

### _escapeString
Returns a [JSON](http://json.org) serialization of an object.

### _fade
Returns an animation that will fade the node defined by
args.node from the start to end values passed (args.start
args.end) (end is mandatory, start is optional)

### _filterQueryResult


### _fixIeBiDiScrollLeft
In RTL direction, scrollLeft should be a negative value, but IE
returns a positive one. All codes using documentElement.scrollLeft
must call this function to fix this error, otherwise the position
will offset to right when there is a horizontal scrollbar.

### _gcNodeData
super expensive: GC all data in the data for nodes that no longer exist in the dom.

### _getBorderExtents
returns an object with properties useful for noting the border
dimensions.

### _getContentBox
Returns an object that encodes the width, height, left and top
positions of the node's content box, irrespective of the
current box model.

### _getIeDocumentElementOffset
returns the offset in x and y from the document body to the
visual edge of the page for IE

### _getMarginBox
returns an object that encodes the width, height, left and top
positions of the node's margin box.

### _getMarginExtents
returns object with properties useful for box fitting with
regards to box margins (i.e., the outer-box).

- l/t = marginLeft, marginTop, respectively
- w = total width, margin inclusive
- h = total height, margin inclusive

The w/h are used for calculating boxes.
Normally application code will not need to invoke this
directly, and will use the ...box... functions instead.

### _getMarginSize
returns an object that encodes the width and height of
the node's margin box

### _getPadBorderExtents
Returns object with properties useful for box fitting with
regards to padding.

### _getPadExtents
Returns object with special values specifically useful for node
fitting.

### _getText
Read the contents of the specified uri and return those contents.

### _inContext


### _ioAddQueryToUrl
Adds query params discovered by the io deferred construction to the URL.
Only use this for operations which are fundamentally GET-type operations.

### _ioCancelAll
Cancels all pending IO requests, regardless of IO type
(xhr, script, iframe).

### _ioNotifyStart
If dojo.publish is available, publish topics
about the start of a request queue and/or the
the beginning of request.

Used by IO transports. An IO transport should
call this method before making the network connection.

### _ioSetArgs
sets up the Deferred and ioArgs property on the Deferred so it
can be used in an io call.

### _ioWatch
Watches the io request represented by dfd to see if it completes.

### _isBodyLtr
Returns true if the current language is left-to-right, and false otherwise.

### _isDocumentOk


### _keypress


### _loadInit


### _loadUri


### _nodeData
Private helper for dojo/NodeList.data for single node data access. Refer to NodeList.data
documentation for more information.


### _removeNodeData
Remove some data from this node

### _spidermonkeyCurrentFile


### _toDom
instantiates an HTML fragment returning the corresponding DOM.

### _xhrObj
does the work of portably generating a new XMLHTTPRequest object.

### addClass
Adds the specified classes to the end of the class list on the
passed node. Will not re-apply duplicate classes.


### addOnLoad
Add a function to execute on DOM content loaded and all requested modules have arrived and been evaluated.
In most cases, the `domReady` plug-in should suffice and this method should not be needed.

When called in a non-browser environment, just checks that all requested modules have arrived and been
evaluated.

### addOnUnload
registers a function to be triggered when the page unloads.

### addOnWindowUnload
registers a function to be triggered when window.onunload fires.
Be careful trying to modify the DOM or access JavaScript properties
during this phase of page unloading: they may not always be available.
Consider dojo.addOnUnload() if you need to modify the DOM or do heavy
JavaScript work.

### anim
A simpler interface to `animateProperty()`, also returns
an instance of `Animation` but begins the animation
immediately, unlike nearly every other Dojo animation API.

### animateProperty
Returns an animation that will transition the properties of
node defined in `args` depending how they are defined in
`args.properties`


### attr
Gets or sets an attribute on an HTML element.

### blendColors
Blend colors end and start with weight from 0 to 1, 0.5 being a 50/50 blend,
can reuse a previously allocated Color object for the result

### body
Return the body element of the specified document or of dojo/_base/window::doc.

### byId
Returns DOM node with matching `id` attribute or falsy value (ex: null or undefined)
if not found.  If `id` is a DomNode, this function is a no-op.


### cache
A getter and setter for storing the string content associated with the
module and url arguments.

### clearCache


### colorFromArray
Builds a `Color` from a 3 or 4 element array, mapping each
element in sequence to the rgb(a) values of the color.

### colorFromHex
Converts a hex string with a '#' prefix to a color object.
Supports 12-bit #rgb shorthand. Optionally accepts a
`Color` object to update with the parsed value.


### colorFromRgb
get rgb(a) array from css-style color declarations

### colorFromString
Parses `str` for a color value. Accepts hex, rgb, and rgba
style color values.

### connect
`dojo.connect` is a deprecated event handling and delegation method in
Dojo. It allows one function to "listen in" on the execution of
any other, triggering the second whenever the first is called. Many
listeners may be attached to a function, and source functions may
be either regular function calls or DOM events.


### contentBox
Getter/setter for the content-box of node.

### cookie
Get or set a cookie.

### coords
Deprecated: Use position() for border-box x/y/w/h
or marginBox() for margin-box w/h/l/t.

Returns an object that measures margin-box (w)idth/(h)eight
and absolute position x/y of the border-box. Also returned
is computed (l)eft and (t)op values in pixels from the
node's offsetParent as returned from marginBox().
Return value will be in the form:

    { l: 50, t: 200, w: 300: h: 150, x: 100, y: 300 }

Does not act as a setter. If includeScroll is passed, the x and
y params are affected as one would expect in dojo.position().

### create
Create an element, allowing for optional attribute decoration
and placement.

### declare
Create a feature-rich constructor from compact notation.

### deprecated
Log a debug message to indicate that a behavior has been
deprecated.

### destroy


### disconnect
Remove a link created by dojo.connect.

### docScroll
Returns an object with {node, x, y} with corresponding offsets.

### empty


### eval
A legacy method created for use exclusively by internal Dojo methods. Do not use this method
directly unless you understand its possibly-different implications on the platforms your are targeting.

### every
Determines whether or not every item in arr satisfies the
condition implemented by callback.

### exit


### experimental
Marks code as experimental.

### fadeIn
Returns an animation that will fade node defined in 'args' from
its current opacity to fully opaque.

### fadeOut
Returns an animation that will fade node defined in 'args'
from its current opacity to fully transparent.

### fieldToObject
Serialize a form field to a JavaScript object.

### filter
Returns a new Array with those items from arr that match the
condition implemented by callback.

### fixEvent
normalizes properties on the event object including event
bubbling methods, keystroke normalization, and x/y positions

### fixIeBiDiScrollLeft
In RTL direction, scrollLeft should be a negative value, but IE
returns a positive one. All codes using documentElement.scrollLeft
must call this function to fix this error, otherwise the position
will offset to right when there is a horizontal scrollbar.

### forEach
for every item in arr, callback is invoked. Return values are ignored.
If you want to break out of the loop, consider using array.every() or array.some().
forEach does not allow breaking out of the loop over the items in arr.

### formToJson
Create a serialized JSON string from a form node or string
ID identifying the form to serialize

### formToObject
Serialize a form node to a JavaScript object.

### formToQuery
Returns a URL-encoded string representing the form passed as either a
node or string ID identifying the form to serialize

### fromJson
Parses a JavaScript expression and returns a JavaScript value.

### getAttr
Gets an attribute on an HTML element.

### getBorderExtents
returns an object with properties useful for noting the border
dimensions.

### getComputedStyle
Returns a "computed style" object.


### getContentBox
Returns an object that encodes the width, height, left and top
positions of the node's content box, irrespective of the
current box model.

### getIeDocumentElementOffset
returns the offset in x and y from the document body to the
visual edge of the page for IE

### getL10nName


### getMarginBox
returns an object that encodes the width, height, left and top
positions of the node's margin box.

### getMarginExtents
returns object with properties useful for box fitting with
regards to box margins (i.e., the outer-box).

- l/t = marginLeft, marginTop, respectively
- w = total width, margin inclusive
- h = total height, margin inclusive

The w/h are used for calculating boxes.
Normally application code will not need to invoke this
directly, and will use the ...box... functions instead.

### getMarginSize
returns an object that encodes the width and height of
the node's margin box

### getNodeProp
Returns an effective value of a property or an attribute.

### getPadBorderExtents
Returns object with properties useful for box fitting with
regards to padding.

### getPadExtents
Returns object with special values specifically useful for node
fitting.

### getProp
Gets a property on an HTML element.

### getStyle
Accesses styles on a node.

### hasAttr
Returns true if the requested attribute is specified on the
given element, and false otherwise.

### hasClass
Returns whether or not the specified classes are a portion of the
class list currently applied to the node.

### hash
Gets or sets the hash string in the browser URL.

### indexOf
locates the first index of the provided value in the
passed array. If the value is not found, -1 is returned.

### isBodyLtr
Returns true if the current language is left-to-right, and false otherwise.

### isCopyKey
Checks an event for the copy key (meta on Mac, and ctrl anywhere else)

### isDescendant
Returns true if node is a descendant of ancestor

### lastIndexOf
locates the last index of the provided value in the passed
array. If the value is not found, -1 is returned.

### loadInit


### map
applies callback to each element of arr and returns
an Array with the results

### marginBox
Getter/setter for the margin-box of node.

### moduleUrl
Returns a URL relative to a module.

### objectToQuery
takes a name/value mapping object and returns a string representing
a URL-encoded version of that object.

### place
Attempt to insert node into the DOM, choosing from various positioning options.
Returns the first argument resolved to a DOM node.

### platformRequire
require one or more modules based on which host environment
Dojo is currently operating in

### popContext
If the context stack contains elements, ensure that
subsequent code executes in the *previous* context to the
current context. The current context set ([global,
document]) is returned.

### position
Gets the position and size of the passed element relative to
the viewport (if includeScroll==false), or relative to the
document root (if includeScroll==true).


### prop
Gets or sets a property on an HTML element.

### provide


### pushContext
causes subsequent calls to Dojo methods to assume the
passed object and, optionally, document as the default
scopes to use. A 2-element array of the previous global and
document are returned.

### queryToObject
Create an object representing a de-serialized query section of a
URL. Query keys with multiple values are returned in an array.


### rawXhrPost
Sends an HTTP POST request to the server. In addition to the properties
listed for the dojo.__XhrArgs type, the following property is allowed:

### rawXhrPut
Sends an HTTP PUT request to the server. In addition to the properties
listed for the dojo.__XhrArgs type, the following property is allowed:

### ready
Add a function to execute on DOM content loaded and all requested modules have arrived and been evaluated.
In most cases, the `domReady` plug-in should suffice and this method should not be needed.

When called in a non-browser environment, just checks that all requested modules have arrived and been
evaluated.

### registerModulePath
Maps a module name to a path

### removeAttr
Removes an attribute from an HTML element.

### removeClass
Removes the specified classes from node. No `contains()`
check is required.


### replaceClass
Replaces one or more classes on a node if not present.
Operates more quickly than calling dojo.removeClass and dojo.addClass


### require
loads a Javascript module from the appropriate URI


### requireAfterIf
If the condition is true then call `dojo.require()` for the specified
resource


### requireIf
If the condition is true then call `dojo.require()` for the specified
resource


### requireLocalization


### safeMixin
Mix in properties skipping a constructor and decorating functions
like it is done by declare().

### setAttr
Sets an attribute on an HTML element.

### setContentSize
Sets the size of the node's contents, irrespective of margins,
padding, or borders.

### setContext
changes the behavior of many core Dojo functions that deal with
namespace and DOM lookup, changing them to work in a new global
context (e.g., an iframe). The varibles dojo.global and dojo.doc
are modified as a result of calling this function and the result of
`dojo.body()` likewise differs.

### setMarginBox
sets the size of the node's margin box and placement
(left/top), irrespective of box model. Think of it as a
passthrough to setBox that handles box-model vagaries for
you.

### setProp
Sets a property on an HTML element.

### setSelectable
Enable or disable selection on a node

### setStyle
Sets styles on a node.

### some
Determines whether or not any item in arr satisfies the
condition implemented by callback.

### stopEvent
prevents propagation and clobbers the default action of the
passed event

### style
Accesses styles on a node. If 2 arguments are
passed, acts as a getter. If 3 arguments are passed, acts
as a setter.

### toDom
instantiates an HTML fragment returning the corresponding DOM.

### toJson
Returns a [JSON](http://json.org) serialization of an object.

### toPixelValue
converts style value to pixels on IE or return a numeric value.

### toggleClass
Adds a class to node if not present, or removes if present.
Pass a boolean condition if you want to explicitly add or remove.
Returns the condition that was specified directly or indirectly.


### unsubscribe
Remove a topic listener.

### when
Transparently applies callbacks to values and/or promises.

### windowUnloaded
signal fired by impending window destruction. You may use
dojo.addOnWIndowUnload() or dojo.connect() to this method to perform
page/application cleanup methods. See dojo.addOnWindowUnload for more info.

### withDoc
Invoke callback with documentObject as dojo/_base/window::doc.

### withGlobal
Invoke callback with globalObject as dojo.global and
globalObject.document as dojo.doc.

### xhr
Deprecated.   Use dojo/request instead.

### xhrDelete
Sends an HTTP DELETE request to the server.

### xhrGet
Sends an HTTP GET request to the server.

### xhrPost
Sends an HTTP POST request to the server. In addition to the properties
listed for the dojo.__XhrArgs type, the following property is allowed:

### xhrPut
Sends an HTTP PUT request to the server. In addition to the properties
listed for the dojo.__XhrArgs type, the following property is allowed:

## Static Methods

### hasOwnProperty


### toString


