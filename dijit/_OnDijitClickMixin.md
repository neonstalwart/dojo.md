# Module: dijit/_OnDijitClickMixin

*Constructor*

## Properties

### a11yclick
Custom press, release, and click synthetic events
which trigger on a left mouse click, touch, or space/enter keyup.

# Constructor

## Summary

Deprecated.   New code should access the dijit/a11yclick event directly, ex:

      this.own(on(node, a11yclick, function(){ ... }));


Mixing in this class will make _WidgetBase.connect(node, "ondijitclick", ...) work.
It also used to be necessary to make templates with ondijitclick work, but now you can just require
dijit/a11yclick.
## Properties

### declaredClass


## Methods

### connect


