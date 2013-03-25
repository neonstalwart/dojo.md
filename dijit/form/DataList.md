# Module: dijit/form/DataList

*Constructor*

# Constructor

## Summary

Inefficient but small data store specialized for inlined data via OPTION tags

## Description

Provides a store for inlined data like:


    <datalist>
    <option value="AL">Alabama</option>
    ...
## Properties

### data
The array of all the objects in the memory store

### declaredClass


### idProperty
Indicates the property to use as the identity property. The values of this
property should be unique.

### index
An index of data indices into the data array by id

## Methods

### add
Creates an object, throws an error if the object already exists

### destroy


### fetchSelectedItem
Get the option marked as selected, like `<option selected>`.
Not part of dojo.data API.

### get
Retrieves an object by its identity

### getChildren
Retrieves the children of an object.

### getIdentity
Returns an object's identity

### getMetadata
Returns any metadata about the object. This may include attribution,
cache directives, history, or version information.

### put
Stores an object

### query
Queries the store for objects.

### queryEngine
Defines the query engine to use for querying the data store

### remove
Deletes an object by its identity

### setData
Sets the given data as the source for this store, and indexes it

### transaction
Starts a new transaction.
Note that a store user might not call transaction() prior to using put,
delete, etc. in which case these operations effectively could be thought of
as "auto-commit" style actions.

