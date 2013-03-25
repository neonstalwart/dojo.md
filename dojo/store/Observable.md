# Module: dojo/store/Observable

## Summary

The Observable store wrapper takes a store and sets an observe method on query()
results that can be used to monitor results for changes.

## Description

Observable wraps an existing store so that notifications can be made when a query
is performed.

## Examples

Create a Memory store that returns an observable query, and then log some
information about that query.


      var store = Observable(new Memory({
        data: [
          {id: 1, name: "one", prime: false},
          {id: 2, name: "two", even: true, prime: true},
          {id: 3, name: "three", prime: true},
          {id: 4, name: "four", even: true, prime: false},
          {id: 5, name: "five", prime: true}
        ]
      }));
      var changes = [], results = store.query({ prime: true });
      var observer = results.observe(function(object, previousIndex, newIndex){
        changes.push({previousIndex:previousIndex, newIndex:newIndex, object:object});
      });


See the Observable tests for more information.
