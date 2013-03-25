# Module: dijit/_Templated

*Constructor*

# Constructor

## Summary

Deprecated mixin for widgets that are instantiated from a template.
Widgets should use _TemplatedMixin plus if necessary _WidgetsInTemplateMixin instead.
## Properties

### attachScope
Object to which attach points and events will be scoped.  Defaults
to 'this'.

### contextRequire
Used to provide a context require to the dojo/parser in order to be
able to use relative MIDs (e.g. `./Widget`) in the widget's template.

### declaredClass


### searchContainerNode


### templatePath
Path to template (HTML file) for this widget relative to dojo.baseUrl.
Deprecated: use templateString with require([... "dojo/text!..."], ...) instead

### templateString
A string that represents the widget template.
Use in conjunction with dojo.cache() to load from a file.

### widgetsInTemplate
Should we parse the template to find widgets that might be
declared in markup inside it?  False by default.

## Methods

### buildRendering
Construct the UI for this widget from a template, setting this.domNode.

### destroyRendering


### startup


