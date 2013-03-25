# Module: dijit/form/_SearchMixin

*Constructor*

# Constructor

**,*protected*

## Summary

A mixin that implements the base functionality to search a store based upon user-entered text such as
with `dijit/form/ComboBox` or `dijit/form/FilteringSelect`
## Properties

### declaredClass


### fetchProperties
Mixin to the store's fetch.
For example, to set the sort order of the ComboBox menu, pass:

      { sort: [{attribute:"name",descending: true}] }

To override the default queryOptions so that deep=false, do:

      { queryOptions: {ignoreCase: true, deep: false} }

### ignoreCase
Set true if the query should ignore case when matching possible items

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

### onSearch
Callback when a search completes.


### postMixInProperties


