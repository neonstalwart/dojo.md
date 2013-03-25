# Module: dojo/NodeList

## Summary

Array-like object which adds syntactic
sugar for chaining, common iteration operations, animation, and
node manipulation. NodeLists are most often returned as the
result of dojo.query() calls.
## Description

NodeList instances provide many utilities that reflect
core Dojo APIs for Array iteration and manipulation, DOM
manipulation, and event handling. Instead of needing to dig up
functions in the dojo.* namespace, NodeLists generally make the
full power of Dojo available for DOM manipulation tasks in a
simple, chainable way.
## Properties

### _nodeDataCache


### events


## Methods

### _adaptAsFilter
adapts a single node function to be used in the filter-type actions

### _adaptAsForEach
adapts a single node function to be used in the forEach-type
actions. The initial object is returned from the specialized
function.

### _adaptAsMap
adapts a single node function to be used in the map-type
actions. The return is a new array of values, as via `dojo.map`

### _adaptWithCondition
adapts a single node function to be used in the map-type
actions, behaves like forEach() or map() depending on arguments

### _gcNodeData
super expensive: GC all data in the data for nodes that no longer exist in the dom.

### _wrap
decorate an array to make it look like a `dojo/NodeList`.

# Constructor

## Methods

### _NodeListCtor
Array-like object which adds syntactic
sugar for chaining, common iteration operations, animation, and
node manipulation. NodeLists are most often returned as the
result of dojo.query() calls.

### _anim


### _buildArrayFromCallback
builds a new array of possibly differing size based on the input list.
Since the returned array is likely of different size than the input array,
the array's map function cannot be used.

### _cloneNode
private utility to clone a node. Not very interesting in the vanilla
dojo/NodeList case, but delegates could do interesting things like
clone event handlers if that is derivable from the node.

### _getRelatedUniqueNodes
cycles over all the nodes and calls a callback
to collect nodes for a possible inclusion in a result.
The callback will get two args: callback(node, ary),
where ary is the array being used to collect the nodes.

### _getUniqueAsNodeList
given a list of nodes, make sure only unique
elements are returned as our NodeList object.
Does not call _stash().

### _getUniqueNodeListWithParent
gets unique element nodes, filters them further
with an optional query and then calls _stash to track parent NodeList.

### _normalize
normalizes data to an array of items to insert.

### _place
private utility to handle placing an array of nodes relative to another node.

### _placeMultiple
private method for inserting queried nodes into all nodes in this NodeList
at different positions. Differs from NodeList.place because it will clone
the nodes in this NodeList if the query matches more than one element.

### _stash
private function to hold to a parent NodeList. end() to return the parent NodeList.


### _wrap
decorate an array to make it look like a `dojo/NodeList`.

### addClass
adds the specified class to every node in the list

### addContent
add a node, NodeList or some HTML as a string to every item in the
list.  Returns the original list.

### adopt
places any/all elements in queryOrListOrNode at a
position relative to the first element in this list.
Returns a dojo/NodeList of the adopted elements.

### after
Places the content after every node in the NodeList.

### andSelf
Adds the nodes from the previous dojo/NodeList to the current dojo/NodeList.

### anim
Animate one or more CSS properties for all nodes in this list.
The returned animation object will already be playing when it
is returned. See the docs for `dojo.anim` for full details.

### animateProperty
Animate all elements of this NodeList across the properties specified.
syntax identical to `dojo.animateProperty`


### append
appends the content to every node in the NodeList.

### appendTo
appends nodes in this NodeList to the nodes matched by
the query passed to appendTo.

### at
Returns a new NodeList comprised of items in this NodeList
at the given index or indices.


### attr
gets or sets the DOM attribute for every element in the
NodeList. See also `dojo.attr`

### before
Places the content before every node in the NodeList.

### children
Returns all immediate child elements for nodes in this dojo/NodeList.
Optionally takes a query to filter the child elements.

### clone
Clones all the nodes in this NodeList and returns them as a new NodeList.

### closest
Returns closest parent that matches query, including current node in this
dojo/NodeList if it matches the query.

### concat
Returns a new NodeList comprised of items in this NodeList
as well as items passed in as parameters

### connect
Attach event handlers to every item of the NodeList. Uses dojo.connect()
so event properties are normalized.

Application must manually require() "dojo/_base/connect" before using this method.

### coords
Deprecated: Use position() for border-box x/y/w/h
or marginBox() for margin-box w/h/l/t.
Returns the box objects of all elements in a node list as
an Array (*not* a NodeList). Acts like `domGeom.coords`, though assumes
the node passed is each node in this list.

### data
stash or get some arbitrary data on/from these nodes.


### empty
clears all content from each node in the list. Effectively
equivalent to removing all child nodes from every item in
the list.

### end
Ends use of the current `NodeList` by returning the previous NodeList
that generated the current NodeList.

### even
Returns the even nodes in this dojo/NodeList as a dojo/NodeList.

### every
see `dojo.every()` and the [Array.every
docs](https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/every).
Takes the same structure of arguments and returns as
dojo.every() with the caveat that the passed array is
implicitly this NodeList

### fadeIn
fade in all elements of this NodeList via `dojo.fadeIn`


### fadeOut
fade out all elements of this NodeList via `dojo.fadeOut`


### filter
"masks" the built-in javascript filter() method (supported
in Dojo via `dojo.filter`) to support passing a simple
string filter in addition to supporting filtering function
objects.

### first
Returns the first node in this dojo/NodeList as a dojo/NodeList.

### forEach
see `dojo.forEach()`. The primary difference is that the acted-on
array is implicitly this NodeList. If you want the option to break out
of the forEach loop, use every() or some() instead.

### html
allows setting the innerHTML of each node in the NodeList,
if there is a value passed in, otherwise, reads the innerHTML value of the first node.

### indexOf
see dojo.indexOf(). The primary difference is that the acted-on
array is implicitly this NodeList

### innerHTML
allows setting the innerHTML of each node in the NodeList,
if there is a value passed in, otherwise, reads the innerHTML value of the first node.

### insertAfter
The nodes in this NodeList will be placed after the nodes
matched by the query passed to insertAfter.

### insertBefore
The nodes in this NodeList will be placed after the nodes
matched by the query passed to insertAfter.

### instantiate
Create a new instance of a specified class, using the
specified properties and each node in the NodeList as a
srcNodeRef.

### last
Returns the last node in this dojo/NodeList as a dojo/NodeList.

### lastIndexOf
see dojo.lastIndexOf(). The primary difference is that the
acted-on array is implicitly this NodeList

### map
see dojo.map(). The primary difference is that the acted-on
array is implicitly this NodeList and the return is a
NodeList (a subclass of Array)

### marginBox
Returns margin-box size of nodes

### next
Returns the next element for nodes in this dojo/NodeList.
Optionally takes a query to filter the next elements.

### nextAll
Returns all sibling elements that come after the nodes in this dojo/NodeList.
Optionally takes a query to filter the sibling elements.

### odd
Returns the odd nodes in this dojo/NodeList as a dojo/NodeList.

### on
Listen for events on the nodes in the NodeList. Basic usage is:

    query(".my-class").on("click", listener);

This supports event delegation by using selectors as the first argument with the event names as
pseudo selectors. For example:

    dojo.query("#my-list").on("li:click", listener);

This will listen for click events within `<li>` elements that are inside the `#my-list` element.
Because on supports CSS selector syntax, we can use comma-delimited events as well:

    dojo.query("#my-list").on("li button:mouseover, li:click", listener);

### orphan
removes elements in this list that match the filter
from their parents and returns them as a new NodeList.

### parent
Returns immediate parent elements for nodes in this dojo/NodeList.
Optionally takes a query to filter the parent elements.

### parents
Returns all parent elements for nodes in this dojo/NodeList.
Optionally takes a query to filter the child elements.

### place
places elements of this node list relative to the first element matched
by queryOrNode. Returns the original NodeList. See: `dojo.place`

### position
Returns border-box objects (x/y/w/h) of all elements in a node list
as an Array (*not* a NodeList). Acts like `dojo.position`, though
assumes the node passed is each node in this list.

### prepend
prepends the content to every node in the NodeList.

### prependTo
prepends nodes in this NodeList to the nodes matched by
the query passed to prependTo.

### prev
Returns the previous element for nodes in this dojo/NodeList.
Optionally takes a query to filter the previous elements.

### prevAll
Returns all sibling elements that come before the nodes in this dojo/NodeList.
Optionally takes a query to filter the sibling elements.

### query
Returns a new list whose members match the passed query,
assuming elements of the current NodeList as the root for
each search.

### remove
removes elements in this list that match the filter
from their parents and returns them as a new NodeList.

### removeAttr
Removes an attribute from each node in the list.

### removeClass
removes the specified class from every node in the list

### removeData
Remove the data associated with these nodes.

### replaceAll
replaces nodes matched by the query passed to replaceAll with the nodes
in this NodeList.

### replaceClass
Replaces one or more classes on a node if not present.
Operates more quickly than calling `removeClass()` and `addClass()`

### replaceWith
Replaces each node in ths NodeList with the content passed to replaceWith.

### siblings
Returns all sibling elements for nodes in this dojo/NodeList.
Optionally takes a query to filter the sibling elements.

### slice
Returns a new NodeList, maintaining this one in place

### slideTo
slide all elements of the node list to the specified place via `dojo/fx.slideTo()`


### some
Takes the same structure of arguments and returns as
`dojo.some()` with the caveat that the passed array is
implicitly this NodeList.  See `dojo.some()` and Mozilla's
[Array.some
documentation](https://developer.mozilla.org/en/JavaScript/Reference/Global_Objects/Array/some).

### splice
Returns a new NodeList, manipulating this NodeList based on
the arguments passed, potentially splicing in new elements
at an offset, optionally deleting elements

### style
gets or sets the CSS property for every element in the NodeList

### text
allows setting the text value of each node in the NodeList,
if there is a value passed in, otherwise, returns the text value for all the
nodes in the NodeList in one string.

### toString


### toggleClass
Adds a class to node if not present, or removes if present.
Pass a boolean condition if you want to explicitly add or remove.

### val
If a value is passed, allows seting the value property of form elements in this
NodeList, or properly selecting/checking the right value for radio/checkbox/select
elements. If no value is passed, the value of the first node in this NodeList
is returned.

### wipeIn
wipe in all elements of this NodeList via `dojo/fx.wipeIn()`


### wipeOut
wipe out all elements of this NodeList via `dojo/fx.wipeOut()`


### wrap
Wrap each node in the NodeList with html passed to wrap.

### wrapAll
Insert html where the first node in this NodeList lives, then place all
nodes in this NodeList as the child of the html.

### wrapInner
For each node in the NodeList, wrap all its children with the passed in html.

