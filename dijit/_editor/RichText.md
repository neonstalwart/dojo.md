# Module: dijit/_editor/RichText

*Constructor*

# Constructor

**,*private*

## Summary

dijit/_editor/RichText is the core of dijit.Editor, which provides basic
WYSIWYG editing features.

## Description

dijit/_editor/RichText is the core of dijit.Editor, which provides basic
WYSIWYG editing features. It also encapsulates the differences
of different js engines for various browsers.  Do not use this widget
with an HTML &lt;TEXTAREA&gt; tag, since the browser unescapes XML escape characters,
like &lt;.  This can have unexpected behavior and lead to security issues
such as scripting attacks.

## Properties

### active
True if mouse was pressed while over this widget, and hasn't been released yet

### attributeMap
Deprecated.  Instead of attributeMap, widget should have a _setXXXAttr attribute
for each XXX attribute to be mapped to the DOM.

attributeMap sets up a "binding" between attributes (aka properties)
of the widget and the widget's DOM.
Changes to widget attributes listed in attributeMap will be
reflected into the DOM.

For example, calling set('title', 'hello')
on a TitlePane will automatically cause the TitlePane's DOM to update
with the new title.

attributeMap is a hash where the key is an attribute of the widget,
and the value reflects a binding to a:

- DOM node attribute

    focus: {node: "focusNode", type: "attribute"}

Maps this.focus to this.focusNode.focus

- DOM node innerHTML

    title: { node: "titleNode", type: "innerHTML" }

Maps this.title to this.titleNode.innerHTML

- DOM node innerText

    title: { node: "titleNode", type: "innerText" }

Maps this.title to this.titleNode.innerText

- DOM node CSS class

    myClass: { node: "domNode", type: "class" }

Maps this.myClass to this.domNode.className

If the value is an array, then each element in the array matches one of the
formats of the above list.

There are also some shorthands for backwards compatibility:

- string --> { node: string, type: "attribute" }, for example:


    "focusNode" ---> { node: "focusNode", type: "attribute" }


- "" --> { node: "domNode", type: "attribute" }

### baseClass


### captureEvents
Events which should be connected to the underlying editing
area, events in this array will be addListener with
capture=true.

### class


### containerNode
Designates where children of the source DOM node will be placed.
"Children" in this case refers to both DOM nodes and widgets.
For example, for myWidget:


    <div data-dojo-type=myWidget>
    <b> here's a plain DOM node
    <span data-dojo-type=subWidget>and a widget</span>
    <i> and another plain DOM node </i>
    </div>


containerNode would point to:


    <b> here's a plain DOM node
    <span data-dojo-type=subWidget>and a widget</span>
    <i> and another plain DOM node </i>


In templated widgets, "containerNode" is set via a
data-dojo-attach-point assignment.

containerNode must be defined for any widget that accepts innerHTML
(like ContentPane or BorderContainer or even Button), and conversely
is null for widgets that don't, like TextBox.

### cssStateNodes
Subclasses may define a cssStateNodes property that lists sub-nodes within the widget that
need CSS classes applied on mouse hover/press and focus.

Each entry in this optional hash is a an attach-point name (like "upArrowButton") mapped to a CSS class name
(like "dijitUpArrowButton"). Example:

    {
    "upArrowButton": "dijitUpArrowButton",
    "downArrowButton": "dijitDownArrowButton"
    }

The above will set the CSS class dijitUpArrowButton to the this.upArrowButton DOMNode when it
is hovered, etc.

### declaredClass


### dir
Bi-directional support, as defined by the [HTML DIR](http://www.w3.org/TR/html401/struct/dirlang.html#adef-dir)
attribute. Either left-to-right "ltr" or right-to-left "rtl".  If undefined, widgets renders in page's
default direction.

### disableSpellCheck
When true, disables the browser's native spell checking, if supported.
Works only in Firefox.

### disabled
The editor is disabled; the text cannot be changed.

### domNode
This is our visible representation of the widget! Other DOM
Nodes may by assigned to other properties, usually through the
template system's data-dojo-attach-point syntax, but the domNode
property is the canonical "top level" node in widget UI.

### events
events which should be connected to the underlying editing area

### focusOnLoad
Focus into this widget when the page is loaded

### focused
This widget or a widget it contains has focus, or is "active" because
it was recently clicked.

### height
Set height to fix the editor at a specific height, with scrolling.
By default, this is 300px.  If you want to have the editor always
resizes to accommodate the content, use AlwaysShowToolbar plugin
and set height="".  If this editor is used within a layout widget,
set height="100%".

### hovering
True if cursor is over this widget

### id
A unique, opaque ID string that can be assigned by users or by the
system. If the developer passes an ID which is known not to be
unique, the specified ID is ignored and the system-generated ID is
used instead.

### inheritWidth
whether to inherit the parent's width or simply use 100%

### isClosed


### isLoaded


### isTabIndent
Make tab key and shift-tab indent and outdent rather than navigating.
Caution: sing this makes web pages inaccessible to users unable to use a mouse.

### lang
Rarely used.  Overrides the default Dojo locale used to render this widget,
as defined by the [HTML LANG](http://www.w3.org/TR/html401/struct/dirlang.html#adef-lang) attribute.
Value must be among the list of locales specified during by the Dojo bootstrap,
formatted according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt) (like en-us).

### minHeight
The minimum height that the editor should have.

### name
Specifies the name of a (hidden) `<textarea>` node on the page that's used to save
the editor content on page leave.   Used to restore editor contents after navigating
to a new page and then hitting the back button.

### onLoadDeferred
Deferred which is fired when the editor finishes loading.
Call myEditor.onLoadDeferred.then(callback) it to be informed
when the rich-text area initialization is finalized.

### ownerDocument
The document this widget belongs to.  If not specified to constructor, will default to
srcNodeRef.ownerDocument, or if no sourceRef specified, then to the document global

### srcNodeRef
pointer to original DOM node

### style
HTML style attributes as cssText string or name/value hash

### styleSheets
semicolon (";") separated list of css files for the editing area

### title
HTML title attribute.

For form widgets this specifies a tooltip to display when hovering over
the widget (just like the native HTML title attribute).

For TitlePane or for when this widget is a child of a TabContainer, AccordionContainer,
etc., it's used to specify the tab label, accordion pane title, etc.

### tooltip
When this widget's title attribute is used to for a tab label, accordion pane title, etc.,
this specifies the tooltip to appear when the mouse is hovered over that text.

### updateInterval


## Methods

### addKeyHandler
Add a handler for a keyboard shortcut

### addStyleSheet
add an external stylesheet for the editing area

### attr
Set or get properties on a widget instance.

### blur
Remove focus from this instance.

### buildRendering
Construct the UI for this widget, setting this.domNode.
Most widgets will mixin `dijit._TemplatedMixin`, which implements this method.

### close
Kills the editor and optionally writes back the modified contents to the
element from which it originated.

### connect
Deprecated, will be removed in 2.0, use this.own(on(...)) or this.own(aspect.after(...)) instead.

Connects specified obj/event to specified method of this object
and registers for disconnect() on widget destroy.

Provide widget-specific analog to dojo.connect, except with the
implicit use of this widget as the target object.
Events connected with `this.connect` are disconnected upon
destruction.

### create
Kick off the life-cycle of a widget

### defer
Wrapper to setTimeout to avoid deferred functions executing
after the originating widget has been destroyed.
Returns an object handle with a remove method (that returns null) (replaces clearTimeout).

### destroy


### destroyDescendants
Recursively destroy the children of this widget and their
descendants.

### destroyRecursive
Destroy this widget and its descendants

### destroyRendering
Destroys the DOM nodes associated with this widget.

### disconnect
Deprecated, will be removed in 2.0, use handle.remove() instead.

Disconnects handle created by `connect`.

### emit
Used by widgets to signal that a synthetic event occurred, ex:

    myWidget.emit("attrmodified-selectedChildWidget", {}).


Emits an event on this.domNode named type.toLowerCase(), based on eventObj.
Also calls onType() method, if present, and returns value from that method.
By default passes eventObj to callback, but will pass callbackArgs instead, if specified.
Modifies eventObj by adding missing parameters (bubbles, cancelable, widget).

### escapeXml
Adds escape sequences for special characters in XML.
Optionally skips escapes for single quotes

### execCommand
Executes a command in the Rich Text area

### focus
Move focus to this editor

### get
Get a property from a widget.

### getChildren
Returns all direct children of this widget, i.e. all widgets underneath this.containerNode whose parent
is this widget.   Note that it does not return all descendants, but rather just direct children.
Analogous to [Node.childNodes](https://developer.mozilla.org/en-US/docs/DOM/Node.childNodes),
except containing widgets rather than DOMNodes.

The result intentionally excludes internally created widgets (a.k.a. supporting widgets)
outside of this.containerNode.

Note that the array returned is a simple array.  Application code should not assume
existence of methods like forEach().

### getDescendants
Returns all the widgets contained by this, i.e., all widgets underneath this.containerNode.
This method should generally be avoided as it returns widgets declared in templates, which are
supposed to be internal/hidden, but it's left here for back-compat reasons.

### getFooterHeight
A function for obtaining the height of the footer node

### getHeaderHeight
A function for obtaining the height of the header node

### getNodeChildrenHtml
Deprecated.   Use dijit/_editor/html::getChildrenHtml() instead.

### getNodeHtml
Deprecated.   Use dijit/_editor/html::_getNodeHtml() instead.

### getParent
Returns the parent widget of this widget.

### getValue
Return the current content of the editing area (post filters
are applied).  Users should call get('value') instead.

### isFocusable
Return true if this widget can currently be focused
and false if not

### isLeftToRight
Return this widget's explicit or implicit orientation (true for LTR, false for RTL)

### on


### onBlur
Called when the widget stops being "active" because
focus moved to something outside of it, or the user
clicked somewhere outside of it, or the widget was
hidden.

### onChange
This is fired if and only if the editor loses focus and
the content is changed.

### onClick
Handler for when the user clicks.

### onClose
Called when this widget is being displayed as a popup (ex: a Calendar popped
up from a DateTextBox), and it is hidden.
This is called from the dijit.popup code, and should not be called directly.

Also used as a parameter for children of `dijit/layout/StackContainer` or subclasses.
Callback if a user tries to close the child.   Child will be closed if this function returns true.

### onDblClick
Connect to this function to receive notifications of mouse double click events.

### onDisplayChanged
This event will be fired every time the display context
changes and the result needs to be reflected in the UI.

### onFocus
Called when the widget becomes "active" because
it or a widget inside of it either has focus, or has recently
been clicked.

### onHide
Called when another widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate hide of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### onKeyDown
Handler for keydown event

### onKeyPress
Connect to this function to receive notifications of printable keys being typed.

### onKeyPressed
Handler for after the user has pressed a key, and the display has been updated.
(Runs on a timer so that it runs after the display is updated)

### onKeyUp
Handler for onkeyup event

### onLoad
Handler after the iframe finishes loading.

### onMouseDown
Connect to this function to receive notifications of when the mouse button is pressed down.

### onMouseEnter
Connect to this function to receive notifications of when the mouse moves onto this widget.

### onMouseLeave
Connect to this function to receive notifications of when the mouse moves off of this widget.

### onMouseMove
Connect to this function to receive notifications of when the mouse moves over nodes contained within this widget.

### onMouseOut
Connect to this function to receive notifications of when the mouse moves off of nodes contained within this widget.

### onMouseOver
Connect to this function to receive notifications of when the mouse moves onto nodes contained within this widget.

### onMouseUp
Connect to this function to receive notifications of when the mouse button is released.

### onNormalizedDisplayChanged
This event is fired every updateInterval ms or more

### onShow
Called when this widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate display of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### open
Transforms the node referenced in this.domNode into a rich text editing
node.

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### placeAt
Place this widget somewhere in the DOM based
on standard domConstruct.place() conventions.

### placeCursorAtEnd
Place the cursor at the end of the editing area.

### placeCursorAtStart
Place the cursor at the start of the editing area.

### postCreate


### postMixInProperties
Called after the parameters to the widget have been read-in,
but before the widget template is instantiated. Especially
useful to set properties that are referenced in the widget
template.

### postscript
Kicks off widget instantiation.  See create() for details.

### queryCommandAvailable
Tests whether a command is supported by the host. Clients
SHOULD check whether a command is supported before attempting
to use it, behaviour for unsupported commands is undefined.

### queryCommandEnabled
Check whether a command is enabled or not.

### queryCommandState
Check the state of a given command and returns true or false.

### queryCommandValue
Check the value of a given command. This matters most for
custom selections and complex values like font value setting.

### removeStyleSheet
remove an external stylesheet for the editing area

### replaceValue
This function set the content while trying to maintain the undo stack
(now only works fine with Moz, this is identical to setValue in all
other browsers)

### set
Set a property on a widget

### setAttribute
Deprecated.  Use set() instead.

### setDisabled
Deprecated, use set('disabled', ...) instead.

### setValue
This function sets the content. No undo history is preserved.
Users should use set('value', ...) instead.

### setupDefaultShortcuts
Add some default key handlers

### startup


### subscribe
Deprecated, will be removed in 2.0, use this.own(topic.subscribe()) instead.

Subscribes to the specified topic and calls the specified method
of this object and registers for unsubscribe() on widget destroy.

Provide widget-specific analog to dojo.subscribe, except with the
implicit use of this widget as the target object.

### uninitialize
Deprecated. Override destroy() instead to implement custom widget tear-down
behavior.

### unsubscribe
Deprecated, will be removed in 2.0, use handle.remove() instead.

Unsubscribes handle created by this.subscribe.
Also removes handle from this widget's list of subscriptions

### watch
Watches a property for changes

