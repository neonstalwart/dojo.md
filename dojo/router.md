# Module: dojo/router

## Summary

A singleton-style instance of dojo/router/RouterBase. See that
module for specifics.
## Examples

      router.register("/widgets/:id", function(evt){
        // If "/widgets/3" was matched,
        // evt.params.id === "3"
        xhr.get({
          url: "/some/path/" + evt.params.id,
          load: function(data){
            // ...
          }
        });
      });
