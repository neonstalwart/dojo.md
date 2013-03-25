# Module: dijit/form/ComboBoxMixin

*Constructor*

# Constructor

## Summary

Provides main functionality of ComboBox widget
## Properties

### autoComplete
If user types in a partial string, and then tab out of the `<input>` box,
automatically copy the first entry displayed in the drop down list to
the `<input>` field

### autoWidth
Set to true to make the drop down at least as wide as this
widget.  Set to false if the drop down should just be its
default width

### baseClass


### cssStateNodes


### declaredClass


### dropDown
The widget to display as a popup.  This widget *must* be
defined before the startup function is called.

### dropDownClass
Dropdown widget class used to select a date/time.
Subclasses should specify this.

### dropDownPosition
This variable controls the position of the drop down.
It's an array of strings with the following values:

- before: places drop down to the left of the target node/widget, or to the right in
the case of RTL scripts like Hebrew and Arabic
- after: places drop down to the right of the target node/widget, or to the left in
the case of RTL scripts like Hebrew and Arabic
- above: drop down goes above target node
- below: drop down goes below target node

The list is positions is tried, in order, until a position is found where the drop down fits
within the viewport.


### fetchProperties
Mixin to the store's fetch.
For example, to set the sort order of the ComboBox menu, pass:

      { sort: [{attribute:"name",descending: true}] }

To override the default queryOptions so that deep=false, do:

      { queryOptions: {ignoreCase: true, deep: false} }

### forceWidth
Set to true to make the drop down exactly as wide as this
widget.  Overrides autoWidth.

### hasDownArrow
Set this textbox to have a down arrow button, to display the drop down list.
Defaults to true.

### highlightMatch
One of: "first", "all" or "none".

If the ComboBox/FilteringSelect opens with the search results and the searched
string can be found, it will be highlighted.  If set to "all"
then will probably want to change `queryExpr` parameter to '*${0}*'

Highlighting is only performed when `labelType` is "text", so as to not
interfere with any HTML markup an HTML label might contain.

### ignoreCase
Set true if the query should ignore case when matching possible items

### item
This is the item returned by the dojo/store/api/Store implementation that
provides the data for this ComboBox, it's the currently selected item.

### labelAttr
The entries in the drop down list come from this attribute in the
dojo.data items.
If not specified, the searchAttr attribute is used instead.

### labelType
Specifies how to interpret the labelAttr in the data store items.
Can be "html" or "text".

### maxHeight
The max height for our dropdown.
Any dropdown taller than this will have scrollbars.
Set to 0 for no max height, or -1 to limit height to available space in viewport

### pageSize
Argument to data provider.
Specifies maximum number of search results to return per query

### query
A query that can be passed to `store` to initially filter the items.
ComboBox overwrites any reference to the `searchAttr` and sets it to the `queryExpr` with the user's input substituted.

### queryExpr
This specifies what query is sent to the data store,
based on what the user has typed.  Changing this expression will modify
whether the results are only exact matches, a "starting with" match,
etc.
`${0}` will be substituted for the user text.
`*` is used for wildcards.
`${0}*` means "starts with", `*${0}*` means "contains", `${0}` means "is"

### searchAttr
Search for items in the data store where this attribute (in the item)
matches what the user typed

### searchDelay
Delay in milliseconds between when user types something and we start
searching based on that value

### store
Reference to data provider object used by this ComboBox.

Should be dojo/store/api/Store, but dojo/data/api/Read supported
for backwards compatibility.

### templateString


## Methods

### buildRendering


### closeDropDown
Closes the drop down on this widget

### destroy


### doHighlight
Highlights the string entered by the user in the menu.  By default this
highlights the first occurrence found. Override this method
to implement your custom highlighting.

### isLoaded
Returns true if the dropdown exists and it's data is loaded.  This can
be overridden in order to force a call to loadDropDown().

### labelFunc
Computes the label to display based on the dojo.data store item.

### loadAndOpenDropDown
Creates the drop down if it doesn't exist, loads the data
if there's an href and it hasn't been loaded yet, and
then opens the drop down.  This is basically a callback when the
user presses the down arrow button to open the drop down.

### loadDropDown
Creates the drop down if it doesn't exist, loads the data
if there's an href and it hasn't been loaded yet, and then calls
the given callback.

### onSearch
Callback when a search completes.


### openDropDown
Opens the dropdown for this widget.   To be called only when this.dropDown
has been created and is ready to display (ie, it's data is loaded).

### postCreate
set up nodes and connect our mouse and keyboard events

### postMixInProperties


### reset


### toggleDropDown
Callback when the user presses the down arrow button or presses
the down arrow key to open/close the drop down.
Toggle the drop-down widget; if it is up, close it, if not, open it

