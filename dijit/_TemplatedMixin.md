# Module: dijit/_TemplatedMixin

*Constructor*

## Methods

### getCachedTemplate
Static method to get a template based on the templatePath or
templateString key

# Constructor

## Summary

Mixin for widgets that are instantiated from a template
## Properties

### attachScope
Object to which attach points and events will be scoped.  Defaults
to 'this'.

### declaredClass


### searchContainerNode


### templatePath
Path to template (HTML file) for this widget relative to dojo.baseUrl.
Deprecated: use templateString with require([... "dojo/text!..."], ...) instead

### templateString
A string that represents the widget template.
Use in conjunction with dojo.cache() to load from a file.

## Methods

### buildRendering
Construct the UI for this widget from a template, setting this.domNode.

### destroyRendering


