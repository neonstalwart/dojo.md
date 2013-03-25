# Module: dijit/Tree

*Constructor*

## Properties

### PathError


# Constructor

## Summary

This widget displays hierarchical data from a store.
## Properties

### active
True if mouse was pressed while over this widget, and hasn't been released yet

### attachScope
Object to which attach points and events will be scoped.  Defaults
to 'this'.

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

### autoExpand
Fully expand the tree on load.   Overrides `persist`.

### baseClass


### betweenThreshold
Set to a positive value to allow drag and drop "between" nodes.

If during DnD mouse is over a (target) node but less than betweenThreshold
pixels from the bottom edge, dropping the the dragged node will make it
the next sibling of the target node, rather than the child.

Similarly, if mouse is over a target node but less that betweenThreshold
pixels from the top edge, dropping the dragged node will make it
the target node's previous sibling rather than the target node's child.

### checkAcceptance


### checkItemAcceptance


### childSelector


### childrenAttr
Deprecated.   This information should be specified in the model.
One ore more attributes that holds children of a tree node

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

### dndController
Class to use as as the dnd controller.  Specifying this class enables DnD.
Generally you should specify this as dijit/tree/dndSource.
Setting of dijit/tree/_dndSelector handles selection only (no actual DnD).

### dndParams


### domNode
This is our visible representation of the widget! Other DOM
Nodes may by assigned to other properties, usually through the
template system's data-dojo-attach-point syntax, but the domNode
property is the canonical "top level" node in widget UI.

### dragThreshold
Number of pixels mouse moves before it's considered the start of a drag operation

### focused
This widget or a widget it contains has focus, or is "active" because
it was recently clicked.

### focusedChild
The currently focused child widget, or null if there isn't one

### hovering
True if cursor is over this widget

### id
A unique, opaque ID string that can be assigned by users or by the
system. If the developer passes an ID which is known not to be
unique, the specified ID is ignored and the system-generated ID is
used instead.

### label
Deprecated.  Use dijit/tree/ForestStoreModel directly instead.
Used in conjunction with query parameter.
If a query is specified (rather than a root node id), and a label is also specified,
then a fake root node is created and displayed, with this label.

### lang
Rarely used.  Overrides the default Dojo locale used to render this widget,
as defined by the [HTML LANG](http://www.w3.org/TR/html401/struct/dirlang.html#adef-lang) attribute.
Value must be among the list of locales specified during by the Dojo bootstrap,
formatted according to [RFC 3066](http://www.ietf.org/rfc/rfc3066.txt) (like en-us).

### model
Interface to read tree data, get notifications of changes to tree data,
and for handling drop operations (i.e drag and drop onto the tree)

### multiCharSearchDuration
If multiple characters are typed where each keystroke happens within
multiCharSearchDuration of the previous keystroke,
search for nodes matching all the keystrokes.

For example, typing "ab" will search for entries starting with
"ab" unless the delay between "a" and "b" is greater than multiCharSearchDuration.

### onDndCancel
Parameter to dndController, see `dijit/tree/dndSource.onDndCancel()`.
Generally this doesn't need to be set.

### onDndDrop
Parameter to dndController, see `dijit/tree/dndSource.onDndDrop()`.
Generally this doesn't need to be set.

### openOnClick
If true, clicking a folder node's label will open it, rather than calling onClick()

### openOnDblClick
If true, double-clicking a folder node's label will open it, rather than calling onDblClick()

### ownerDocument
The document this widget belongs to.  If not specified to constructor, will default to
srcNodeRef.ownerDocument, or if no sourceRef specified, then to the document global

### path
Backward compatible singular variant of paths.

### paths
Full paths from rootNode to selected nodes expressed as array of items or array of ids.
Since setting the paths may be asynchronous (because of waiting on dojo.data), set("paths", ...)
returns a Promise to indicate when the set is complete.

### persist
Enables/disables use of cookies for state saving.

### query
Deprecated.  User should specify query to the model directly instead.
Specifies datastore query to return the root item or top items for the tree.

### searchContainerNode


### selectedItem
Backward compatible singular variant of selectedItems.

### selectedItems
The currently selected items in this tree.
This property can only be set (via set('selectedItems', ...)) when that item is already
visible in the tree.   (I.e. the tree has already been expanded to show that node.)
Should generally use `paths` attribute to set the selected items instead.

### showRoot
Should the root node be displayed, or hidden?

### srcNodeRef
pointer to original DOM node

### store
Deprecated.  Use "model" parameter instead.
The store to get data to display in the tree.

### style
HTML style attributes as cssText string or name/value hash

### tabIndex
Tab index of the container; same as HTML tabIndex attribute.
Note then when user tabs into the container, focus is immediately
moved to the first item in the container.

### templatePath
Path to template (HTML file) for this widget relative to dojo.baseUrl.
Deprecated: use templateString with require([... "dojo/text!..."], ...) instead

### templateString


### title
HTML title attribute.

For form widgets this specifies a tooltip to display when hovering over
the widget (just like the native HTML title attribute).

For TitlePane or for when this widget is a child of a TabContainer, AccordionContainer,
etc., it's used to specify the tab label, accordion pane title, etc.

### tooltip
When this widget's title attribute is used to for a tab label, accordion pane title, etc.,
this specifies the tooltip to appear when the mouse is hovered over that text.

## Methods

### attr
Set or get properties on a widget instance.

### buildRendering
Construct the UI for this widget, setting this.domNode.
Most widgets will mixin `dijit._TemplatedMixin`, which implements this method.

### collapseAll
Collapse all nodes in the tree

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

### expandAll
Expand all nodes in the tree

### focus
Default focus() implementation: focus the previously focused child, or first child.
Some applications may want to change this method to focus the [first] selected child.

### focusChild
Focus specified child widget.

### focusFirstChild
Focus the first focusable child in the container.

### focusLastChild
End key pressed; go to last visible node.

### focusNode
Focus on the specified node (which must be visible)

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

### getIconClass
Overridable function to return CSS class name to display icon

### getIconStyle
Overridable function to return CSS styles to display icon

### getItemChildren
Deprecated.   This should be specified on the model itself.

Overridable function that return array of child items of given parent item,
or if parentItem==null then return top items in tree

### getLabel
Overridable function to get the label for a tree node (given the item)

### getLabelClass
Overridable function to return CSS class name to display label

### getLabelStyle
Overridable function to return CSS styles to display label

### getNodesByItem
Returns all tree nodes that refer to an item

### getParent
Returns the parent widget of this widget.

### getRowClass
Overridable function to return CSS class name to display row

### getRowStyle
Overridable function to return CSS styles to display row

### getTooltip
Overridable function to get the tooltip for a tree node (given the item)

### isExpandoNode
check whether a dom node is the expandoNode for a particular TreeNode widget

### isFocusable
Return true if this widget can currently be focused
and false if not

### isLeftToRight
Return this widget's explicit or implicit orientation (true for LTR, false for RTL)

### itemCreator
Returns objects passed to `Tree.model.newItem()` based on DnD nodes
dropped onto the tree.   Developer must override this method to enable
dropping from external sources onto this Tree, unless the Tree.model's items
happen to look like {id: 123, name: "Apple" } with no other attributes.

For each node in nodes[], which came from source, create a hash of name/value
pairs to be passed to Tree.model.newItem().  Returns array of those hashes.

### mayHaveChildren
Deprecated.   This should be specified on the model itself.

Overridable function to tell if an item has or may have children.
Controls whether or not +/- expando icon is shown.
(For efficiency reasons we may not want to check if an element actually
has children until user clicks the expando node)

### on


### onBlur
Called when the widget stops being "active" because
focus moved to something outside of it, or the user
clicked somewhere outside of it, or the widget was
hidden.

### onClick
Callback when a tree node is clicked

### onClose
Callback when a node is closed

### onDblClick
Callback when a tree node is double-clicked

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
Connect to this function to receive notifications of keys being pressed down.

### onKeyPress
Connect to this function to receive notifications of printable keys being typed.

### onKeyUp
Connect to this function to receive notifications of keys being released.

### onKeyboardSearch
When a key is pressed that matches a child item,
this method is called so that a widget can take appropriate action is necessary.

### onLoad
Called when tree finishes loading and expanding.

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

### onOpen
Callback when a node is opened

### onShow
Called when this widget becomes the selected pane in a
`dijit/layout/TabContainer`, `dijit/layout/StackContainer`,
`dijit/layout/AccordionContainer`, etc.

Also called to indicate display of a `dijit.Dialog`, `dijit.TooltipDialog`, or `dijit.TitlePane`.

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### placeAt
Place this widget somewhere in the DOM based
on standard domConstruct.place() conventions.

### postCreate


### postMixInProperties


### postscript
Kicks off widget instantiation.  See create() for details.

### resize


### set
Set a property on a widget

### setAttribute
Deprecated.  Use set() instead.

### startup
Processing after the DOM fragment is added to the document

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

