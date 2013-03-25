# Module: dijit/form/_AutoCompleterMixin

*Constructor*

# Constructor

**,*protected*

## Summary

A mixin that implements the base functionality for `dijit/form/ComboBox`/`dijit/form/FilteringSelect`
## Description

All widgets that mix in dijit/form/_AutoCompleterMixin must extend `dijit/form/_FormValueWidget`.
## Properties

### autoComplete
If user types in a partial string, and then tab out of the `<input>` box,
automatically copy the first entry displayed in the drop down list to
the `<input>` field

### declaredClass


### fetchProperties
Mixin to the store's fetch.
For example, to set the sort order of the ComboBox menu, pass:

      { sort: [{attribute:"name",descending: true}] }

To override the default queryOptions so that deep=false, do:

      { queryOptions: {ignoreCase: true, deep: false} }

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
The store must accept an object hash of properties for its query. See `query` and `queryExpr` for details.

## Methods

### closeDropDown


### doHighlight
Highlights the string entered by the user in the menu.  By default this
highlights the first occurrence found. Override this method
to implement your custom highlighting.

### isLoaded


### labelFunc
Computes the label to display based on the dojo.data store item.

### loadDropDown


### onSearch
Callback when a search completes.


### postCreate
Subclasses must call this method from their postCreate() methods

### postMixInProperties


### reset


