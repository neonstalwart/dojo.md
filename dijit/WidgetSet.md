# Module: dijit/WidgetSet

*Constructor*

# Constructor

## Summary

A set of widgets indexed by id.
Deprecated, will be removed in 2.0.

## Examples

* Create a small list of widgets:

      require(["dijit/WidgetSet", "dijit/registry"],
        function(WidgetSet, registry){
        var ws = new WidgetSet();
        ws.add(registry.byId("one"));
        ws.add(registry.byId("two"));
        // destroy both:
        ws.forEach(function(w){ w.destroy(); });
      });


## Properties

### declaredClass


## Methods

### add
Add a widget to this list. If a duplicate ID is detected, a error is thrown.


### byClass
Reduce this widgetset to a new WidgetSet of a particular `declaredClass`


### byId
Find a widget in this list by it's id.

### every
A synthetic clone of `array.every` acting explicitly on this WidgetSet


### filter
Filter down this WidgetSet to a smaller new WidgetSet
Works the same as `array.filter` and `NodeList.filter`


### forEach
Call specified function for each widget in this set.


### map
Create a new Array from this WidgetSet, following the same rules as `array.map`

### remove
Remove a widget from this WidgetSet. Does not destroy the widget; simply
removes the reference.

### some
A synthetic clone of `array.some` acting explicitly on this WidgetSet


### toArray
Convert this WidgetSet into a true Array


