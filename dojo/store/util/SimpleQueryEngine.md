# Module: dojo/store/util/SimpleQueryEngine

## Summary

Simple query engine that matches using filter functions, named filter
functions or objects by name-value on a query object hash

## Description

The SimpleQueryEngine provides a way of getting a QueryResults through
the use of a simple object hash as a filter.  The hash will be used to
match properties on data objects with the corresponding value given. In
other words, only exact matches will be returned.

This function can be used as a template for more complex query engines;
for example, an engine can be created that accepts an object hash that
contains filtering functions, or a string that gets evaluated, etc.

When creating a new dojo.store, simply set the store's queryEngine
field as a reference to this function.

# Constructor

