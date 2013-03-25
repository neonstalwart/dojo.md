# Module: dojo/parser

## Summary

The Dom/Widget parsing package
## Methods

### _clearCache
Clear cached data.   Used mainly for benchmarking.

### _functionFromScript
Convert a `<script type="dojo/method" args="a, b, c"> ... </script>`
into a function

### _instantiate
Takes array of objects representing nodes, and turns them into class instances and
potentially calls a startup method to allow them to connect with
any children.

### _require
Helper for _scanAMD().  Takes a `<script type=dojo/require>bar: "acme/bar", ...</script>` node,
calls require() to load the specified modules and (asynchronously) assign them to the specified global
variables, and returns a Promise for when that operation completes.

In the example above, it is effectively doing a require(["acme/bar", ...], function(a){ bar = a; }).

### _scanAmd
Scans the DOM for any declarative requires and returns their values.

### construct
Calls new ctor(params, node), where params is the hash of parameters specified on the node,
excluding data-dojo-type and data-dojo-mixins.   Does not call startup().

### instantiate
Takes array of nodes, and turns them into class instances and
potentially calls a startup method to allow them to connect with
any children.

### parse
Scan the DOM for class instances, and instantiate them.

### scan
Scan a DOM tree and return an array of objects representing the DOMNodes
that need to be turned into widgets.

# Constructor

## Methods

### hasOwnProperty


### toString


