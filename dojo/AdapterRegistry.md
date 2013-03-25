# Module: dojo/AdapterRegistry

## Summary

A registry to make contextual calling/searching easier.
## Description

Objects of this class keep list of arrays in the form [name, check,
wrap, directReturn] that are used to determine what the contextual
result of a set of checked arguments is. All check/wrap functions
in this registry should be of the same arity.
## Examples

      // create a new registry
      var reg = new dojo.AdapterRegistry();
      reg.register("handleString",
        dojo.isString,
        function(str){
          // do something with the string here
        }
      );
      reg.register("handleArr",
        dojo.isArray,
        function(arr){
          // do something with the array here
        }
      );
    
      // now we can pass reg.match() *either* an array or a string and
      // the value we pass will get handled by the right function
      reg.match("someValue"); // will call the first function
      reg.match(["someValue"]); // will call the second
## Properties

### pairs


### returnWrappers


# Constructor

## Methods

### match
Find an adapter for the given arguments. If no suitable adapter
is found, throws an exception. match() accepts any number of
arguments, all of which are passed to all matching functions
from the registered pairs.

### register
register a check function to determine if the wrap function or
object gets selected

### unregister
Remove a named adapter from the registry

