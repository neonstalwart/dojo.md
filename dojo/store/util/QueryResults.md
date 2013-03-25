# Module: dojo/store/util/QueryResults

## Summary

A function that wraps the results of a store query with additional
methods.
## Description

QueryResults is a basic wrapper that allows for array-like iteration
over any kind of returned data from a query.  While the simplest store
will return a plain array of data, other stores may return deferreds or
promises; this wrapper makes sure that *all* results can be treated
the same.

Additional methods include `forEach`, `filter` and `map`.
