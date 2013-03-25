# Module: dojo/parser

## Summary

The Dom/Widget parsing package
## Methods

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


