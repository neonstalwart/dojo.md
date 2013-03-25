# Module: dijit/_AttachMixin

*Constructor*

# Constructor

## Summary

Mixin for widgets to attach to dom nodes and setup events via
convenient data-dojo-attach-point and data-dojo-attach-event DOM attributes.

Superclass of _TemplatedMixin, and can also be used standalone when templates are pre-rendered on the
server.

Does not [yet] handle widgets like ContentPane with this.containerNode set.   It should skip
scanning for data-dojo-attach-point and data-dojo-attach-event inside this.containerNode, but it
doesn't.
## Properties

### attachScope
Object to which attach points and events will be scoped.  Defaults
to 'this'.

### declaredClass


### searchContainerNode
Search descendants of this.containerNode for data-dojo-attach-point and data-dojo-attach-event.
Should generally be left false (the default value) both for performance and to avoid failures when
this.containerNode holds other _AttachMixin instances with their own attach points and events.

## Methods

### buildRendering
Attach to DOM nodes marked with special attributes.

### destroyRendering


