# Module: dojo/data/ItemFileReadStore

*Constructor*

# Constructor

## Summary

The ItemFileReadStore implements the dojo/data/api/Read API and reads
data from JSON files that have contents in this format --

      { items: [
        { name:'Kermit', color:'green', age:12, friends:['Gonzo', {_reference:{name:'Fozzie Bear'}}]},
        { name:'Fozzie Bear', wears:['hat', 'tie']},
        { name:'Miss Piggy', pets:'Foo-Foo'}
      ]}

Note that it can also contain an 'identifier' property that specified which attribute on the items
in the array of items that acts as the unique identifier for that item.
## Properties

### clearOnClose
Parameter to allow users to specify if a close call should force a reload or not.
By default, it retains the old behavior of not clearing if close is called.  But
if set true, the store will be reset to default state.  Note that by doing this,
all item handles will become invalid and a new fetch must be issued.

### data


### declaredClass


### failOk
Parameter for specifying that it is OK for the xhrGet call to fail silently.

### hierarchical
Parameter to indicate to process data from the url as hierarchical
(data items can contain other data items in js form).  Default is true
for backwards compatibility.  False means only root items are processed
as items, all child objects outside of type-mapped objects and those in
specific reference format, are left straight JS data objects.

### typeMap


### url


### urlPreventCache
Parameter to allow specifying if preventCache should be passed to the xhrGet call or not when loading data from a url.
Note this does not mean the store calls the server on each fetch, only that the data load has preventCache set as an option.
Added for tracker: #6072

## Methods

### close
See dojo/data/api/Read.close()

### containsValue
See dojo/data/api/Read.containsValue()

### emit


### errorHandler
The error handler when there is an error fetching items.  This function should not be called
directly and is used by simpleFetch.fetch().

### fetch
The simpleFetch mixin is designed to serve as a set of function(s) that can
be mixed into other datastore implementations to accelerate their development.

### fetchHandler
The handler when items are sucessfully fetched.  This function should not be called directly
and is used by simpleFetch.fetch().

### fetchItemByIdentity
See dojo/data/api/Identity.fetchItemByIdentity()

### filter
This method handles the basic filtering needs for ItemFile* based stores.

### getAttributes
See dojo/data/api/Read.getAttributes()

### getFeatures
See dojo/data/api/Read.getFeatures()

### getIdentity
See dojo/data/api/Identity.getIdentity()

### getIdentityAttributes
See dojo/data/api/Identity.getIdentityAttributes()

### getLabel
See dojo/data/api/Read.getLabel()

### getLabelAttributes
See dojo/data/api/Read.getLabelAttributes()

### getValue
See dojo/data/api/Read.getValue()

### getValues
See dojo/data/api/Read.getValues()

### hasAttribute
See dojo/data/api/Read.hasAttribute()

### isItem
See dojo/data/api/Read.isItem()

### isItemLoaded
See dojo/data/api/Read.isItemLoaded()

### loadItem
See dojo/data/api/Read.loadItem()

### on


