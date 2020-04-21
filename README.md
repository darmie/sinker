# sinker

Core utility library for Haxe.

**Requires Haxe 4** (developed with v4.0.5).


## Caveats

- Basically platform-independent, however the main target is HashLink.
- Not yet very well tested.
- Quite unstable!


## Usage

The below enables you to use all features of sinker.

```haxe
import sinker.*;
import sinker.globals.Globals.*;

using sinker.extensions.Index;
```

Note that some standard types (such as `Array`, `UInt`) will be shadowed with sinker types, which are not completely compatible (however you can still cast to the original types with casting methods).


## Types

### UInt

Unsigned integer based on `Int`.  
`#if sinker_debug` checks against negative, otherwise no runtime overhead.

### MaybeUInt

Represents either an `UInt` value or the absense of valid value.

### Array<T>

Abstract over standard `Array<T>` with several additional methods.  
Uses `UInt` as length/indices.  
`#if sinker_debug` does boundary checks when accessing elements.

### Maybe<T>

Abstract over standard `Null<T>` with stricter type cast control and some additional methods.

### Option<T>

Abstract over standard `haxe.ds.Option<T>` with some additional methods.


## Utility classes

### Ints

Static utility methods for `Int`.

### UInts

Static utility methods for `UInt`.

### Floats

Static utility methods for `UInt`.

### Arrays

Static utility methods for `Array<T>`.


## Compilation flags

|flag|description|
|---|---|
|sinker_debug|Enables bound checks for `UInt` values and `Array` indices.|
