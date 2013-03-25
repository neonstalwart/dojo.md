# Module: dojo/_base/declare

## Summary

Create a feature-rich constructor from compact notation.
## Description

Create a constructor using a compact notation for inheritance and
prototype extension.

Mixin ancestors provide a type of multiple inheritance.
Prototypes of mixin ancestors are copied to the new class:
changes to mixin prototypes will not affect classes to which
they have been mixed in.

Ancestors can be compound classes created by this version of
declare(). In complex cases all base classes are going to be
linearized according to C3 MRO algorithm
(see http://www.python.org/download/releases/2.3/mro/ for more
details).

"className" is cached in "declaredClass" property of the new class,
if it was supplied. The immediate super class will be cached in
"superclass" property of the new class.

Methods in "props" will be copied and modified: "nom" property
(the declared name of the method) will be added to all copied
functions to help identify them for the internal machinery. Be
very careful, while reusing methods: if you use the same
function under different names, it can produce errors in some
cases.

It is possible to use constructors created "manually" (without
declare()) as bases. They will be called as usual during the
creation of an instance, their methods will be chained, and even
called by "this.inherited()".

Special property "-chains-" governs how to chain methods. It is
a dictionary, which uses method names as keys, and hint strings
as values. If a hint string is "after", this method will be
called after methods of its base classes. If a hint string is
"before", this method will be called before methods of its base
classes.

If "constructor" is not mentioned in "-chains-" property, it will
be chained using the legacy mode: using "after" chaining,
calling preamble() method before each constructor, if available,
and calling postscript() after all constructors were executed.
If the hint is "after", it is chained as a regular method, but
postscript() will be called after the chain of constructors.
"constructor" cannot be chained "before", but it allows
a special hint string: "manual", which means that constructors
are not going to be chained in any way, and programmer will call
them manually using this.inherited(). In the latter case
postscript() will be called after the construction.

All chaining hints are "inherited" from base classes and
potentially can be overridden. Be very careful when overriding
hints! Make sure that all chained methods can work in a proposed
manner of chaining.

Once a method was chained, it is impossible to unchain it. The
only exception is "constructor". You don't need to define a
method in order to supply a chaining hint.

If a method is chained, it cannot use this.inherited() because
all other methods in the hierarchy will be called automatically.

Usually constructors and initializers of any kind are chained
using "after" and destructors of any kind are chained as
"before". Note that chaining assumes that chained methods do not
return any value: any returned value will be discarded.

## Properties

### __DeclareCreatedObject
dojo/_base/declare() returns a constructor `C`.   `new C()` returns an Object with the following
methods, in addition to the methods and properties specified via the arguments passed to declare().

## Methods

### safeMixin
Mix in properties skipping a constructor and decorating functions
like it is done by declare().

# Constructor

