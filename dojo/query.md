# Module: dojo/query

## Summary

This modules provides DOM querying functionality. The module export is a function
that can be used to query for DOM nodes by CSS selector and returns a NodeList
representing the matching nodes.
## Description

dojo/query is responsible for loading the appropriate query engine and wrapping
its results with a `NodeList`. You can use dojo/query with a specific selector engine
by using it as a plugin. For example, if you installed the sizzle package, you could
use it as the selector engine with:

    require(["dojo/query!sizzle"], function(query){
    query("div")...


The id after the ! can be a module id of the selector engine or one of the following values:

- acme: This is the default engine used by Dojo base, and will ensure that the full
Acme engine is always loaded.

- css2: If the browser has a native selector engine, this will be used, otherwise a
very minimal lightweight selector engine will be loaded that can do simple CSS2 selectors
(by #id, .class, tag, and [name=value] attributes, with standard child or descendant (>)
operators) and nothing more.

- css2.1: If the browser has a native selector engine, this will be used, otherwise the
full Acme engine will be loaded.

- css3: If the browser has a native selector engine with support for CSS3 pseudo
selectors (most modern browsers except IE8), this will be used, otherwise the
full Acme engine will be loaded.

- Or the module id of a selector engine can be used to explicitly choose the selector engine

For example, if you are using CSS3 pseudo selectors in module, you can specify that
you will need support them with:

    require(["dojo/query!css3"], function(query){
    query('#t > h3:nth-child(odd)')...


You can also choose the selector engine/load configuration by setting the query-selector:
For example:

    <script data-dojo-config="query-selector:'css3'" src="dojo.js"></script>


## Methods

### NodeList
Array-like object which adds syntactic
sugar for chaining, common iteration operations, animation, and
node manipulation. NodeLists are most often returned as the
result of dojo.query() calls.

### load
can be used as AMD plugin to conditionally load new query engine

