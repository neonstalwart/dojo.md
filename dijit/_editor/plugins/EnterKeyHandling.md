# Module: dijit/_editor/plugins/EnterKeyHandling

*Constructor*

# Constructor

## Summary

This plugin tries to make all browsers behave consistently with regard to
how ENTER behaves in the editor window.  It traps the ENTER key and alters
the way DOM is constructed in certain cases to try to commonize the generated
DOM and behaviors across browsers.

## Description

This plugin has three modes:

- blockNodeForEnter=BR
- blockNodeForEnter=DIV
- blockNodeForEnter=P

In blockNodeForEnter=P, the ENTER key starts a new
paragraph, and shift-ENTER starts a new line in the current paragraph.
For example, the input:


    first paragraph <shift-ENTER>
    second line of first paragraph <ENTER>
    second paragraph


will generate:


    <p>
    first paragraph
    <br/>
    second line of first paragraph
    </p>
    <p>
    second paragraph
    </p>


In BR and DIV mode, the ENTER key conceptually goes to a new line in the
current paragraph, and users conceptually create a new paragraph by pressing ENTER twice.
For example, if the user enters text into an editor like this:


    one <ENTER>
    two <ENTER>
    three <ENTER>
    <ENTER>
    four <ENTER>
    five <ENTER>
    six <ENTER>


It will appear on the screen as two 'paragraphs' of three lines each.  Markupwise, this generates:

BR:

    one<br/>
    two<br/>
    three<br/>
    <br/>
    four<br/>
    five<br/>
    six<br/>


DIV:

    <div>one</div>
    <div>two</div>
    <div>three</div>
    <div>&nbsp;</div>
    <div>four</div>
    <div>five</div>
    <div>six</div>
## Properties

### blockNodeForEnter
This property decides the behavior of Enter key. It can be either P,
DIV, BR, or empty (which means disable this feature). Anything else
will trigger errors.  The default is 'BR'

See class description for more details.

### blockNodes
Regex for testing if a given tag is a block level (display:block) tag

### bogusHtmlContent
HTML to stick into a new empty block

### button
Pointer to `dijit/form/Button` or other widget (ex: `dijit/form/FilteringSelect`)
that is added to the toolbar to control this plugin.
If not specified, will be created on initialization according to `buttonClass`

### buttonClass
Class of widget (ex: dijit.form.Button or dijit/form/FilteringSelect)
that is added to the toolbar to control this plugin.
This is used to instantiate the button, unless `button` itself is specified directly.

### command
String like "insertUnorderedList", "outdent", "justifyCenter", etc. that represents an editor command.
Passed to editor.execCommand() if `useDefaultCommand` is true.

### declaredClass


### disabled
Flag to indicate if this plugin has been disabled and should do nothing
helps control button state, among other things.  Set via the setter api.

### editor
Points to the parent editor

### iconClassPrefix
The CSS class name for the button node is formed from `iconClassPrefix` and `command`

### useDefaultCommand
If true, this plugin executes by calling Editor.execCommand() with the argument specified in `command`.

## Methods

### connect
Deprecated.  Use this.own() with dojo/on or dojo/aspect.instead.

Make a connect.connect() that is automatically disconnected when this plugin is destroyed.
Similar to `dijit/_Widget.connect()`.

### destroy


### get
Get a property from a plugin.

### getLabel
Returns the label to use for the button

### handleEnterKey
Handler for enter key events when blockNodeForEnter is DIV or P.

### onKeyPressed
Handler for after the user has pressed a key, and the display has been updated.
Connected to RichText's onKeyPressed() method.

### own
Track specified handles and remove/destroy them when this instance is destroyed, unless they were
already removed/destroyed manually.

### removeTrailingBr
If last child of container is a `<br>`, then remove it.

### set
Set a property on a plugin

### setEditor


### setToolbar
Tell the plugin to add it's controller widget (often a button)
to the toolbar.  Does nothing if there is no controller widget.

### updateState
Change state of the plugin to respond to events in the editor.

