# Module: dojo/ready

## Summary

Add a function to execute on DOM content loaded and all requested modules have arrived and been evaluated.
In most cases, the `domReady` plug-in should suffice and this method should not be needed.

When called in a non-browser environment, just checks that all requested modules have arrived and been
evaluated.
## Examples

* Simple DOM and Modules ready syntax

      require(["dojo/ready"], function(ready){
        ready(function(){ alert("Dom ready!"); });
      });


* Using a priority

      require(["dojo/ready"], function(ready){
        ready(2, function(){ alert("low priority ready!"); })
      });


* Using context

      require(["dojo/ready"], function(ready){
        ready(foo, function(){
          // in here, this == foo
        });
      });


* Using dojo/hitch style args:

      require(["dojo/ready"], function(ready){
        var foo = { dojoReady: function(){ console.warn(this, "dojo dom and modules ready."); } };
        ready(foo, "dojoReady");
      });


