github\_url  
hide

# RandomNumberGenerator

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides methods for generating pseudo-random numbers.

classref-introduction-group

## Description

RandomNumberGenerator is a class for generating pseudo-random numbers.
It currently uses [PCG32](https://www.pcg-random.org/).

\*\*Note:\*\* The underlying algorithm is an implementation detail and
should not be depended upon.

To generate a random float number (within a given range) based on a
time-dependent seed:

    var rng = RandomNumberGenerator.new()
    func _ready():
        var my_random_number = rng.randf_range(-10.0, 10.0)

classref-introduction-group

## Tutorials

-   `Random number generation <../tutorials/math/random_number_generation>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **seed** = `0`
`🔗<class_RandomNumberGenerator_property_seed>`

classref-property-setget

-   `void (No return value.)` **set\_seed**(value: `int<class_int>`)
-   `int<class_int>` **get\_seed**()

Initializes the random number generator state based on the given seed
value. A given seed will give a reproducible sequence of pseudo-random
numbers.

\*\*Note:\*\* The RNG does not have an avalanche effect, and can output
similar random streams given similar seeds. Consider using a hash
function to improve your seed quality if they're sourced externally.

\*\*Note:\*\* Setting this property produces a side effect of changing
the internal `state<class_RandomNumberGenerator_property_state>`, so
make sure to initialize the seed *before* modifying the
`state<class_RandomNumberGenerator_property_state>`:

\*\*Note:\*\* The default value of this property is pseudo-random, and
changes when calling
`randomize<class_RandomNumberGenerator_method_randomize>`. The `0` value
documented here is a placeholder, and not the actual default seed.

    var rng = RandomNumberGenerator.new()
    rng.seed = hash("Godot")
    rng.state = 100 # Restore to some previously saved state.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **state** = `0`
`🔗<class_RandomNumberGenerator_property_state>`

classref-property-setget

-   `void (No return value.)` **set\_state**(value: `int<class_int>`)
-   `int<class_int>` **get\_state**()

The current state of the random number generator. Save and restore this
property to restore the generator to a previous state:

    var rng = RandomNumberGenerator.new()
    print(rng.randf())
    var saved_state = rng.state # Store current state.
    print(rng.randf()) # Advance internal state.
    rng.state = saved_state # Restore the state.
    print(rng.randf()) # Prints the same value as in previous.

\*\*Note:\*\* Do not set state to arbitrary values, since the random
number generator requires the state to have certain qualities to behave
properly. It should only be set to values that came from the state
property itself. To initialize the random number generator with
arbitrary input, use `seed<class_RandomNumberGenerator_property_seed>`
instead.

\*\*Note:\*\* The default value of this property is pseudo-random, and
changes when calling
`randomize<class_RandomNumberGenerator_method_randomize>`. The `0` value
documented here is a placeholder, and not the actual default seed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **rand\_weighted**(weights:
`PackedFloat32Array<class_PackedFloat32Array>`)
`🔗<class_RandomNumberGenerator_method_rand_weighted>`

Returns a random index with non-uniform weights. Prints an error and
returns `-1` if the array is empty.

gdscript

var rng = RandomNumberGenerator.new()

var my\_array = \["one", "two", "three", "four"\] var weights =
PackedFloat32Array(\[0.5, 1, 1, 2\])

\# Prints one of the four elements in
<span class="title-ref">my\_array</span>. \# It is more likely to print
"four", and less likely to print "one".
print(my\_array\[rng.rand\_weighted(weights)\])

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **randf**()
`🔗<class_RandomNumberGenerator_method_randf>`

Returns a pseudo-random float between `0.0` and `1.0` (inclusive).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **randf\_range**(from: `float<class_float>`, to:
`float<class_float>`)
`🔗<class_RandomNumberGenerator_method_randf_range>`

Returns a pseudo-random float between `from` and `to` (inclusive).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **randfn**(mean: `float<class_float>` = 0.0,
deviation: `float<class_float>` = 1.0)
`🔗<class_RandomNumberGenerator_method_randfn>`

Returns a
[normally-distributed](https://en.wikipedia.org/wiki/Normal_distribution),
pseudo-random floating-point number from the specified `mean` and a
standard `deviation`. This is also known as a Gaussian distribution.

\*\*Note:\*\* This method uses the [Box-Muller
transform](https://en.wikipedia.org/wiki/Box%E2%80%93Muller_transform)
algorithm.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **randi**()
`🔗<class_RandomNumberGenerator_method_randi>`

Returns a pseudo-random 32-bit unsigned integer between `0` and
`4294967295` (inclusive).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **randi\_range**(from: `int<class_int>`, to:
`int<class_int>`) `🔗<class_RandomNumberGenerator_method_randi_range>`

Returns a pseudo-random 32-bit signed integer between `from` and `to`
(inclusive).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **randomize**()
`🔗<class_RandomNumberGenerator_method_randomize>`

Sets up a time-based seed for this **RandomNumberGenerator** instance.
Unlike the `@GlobalScope<class_@GlobalScope>` random number generation
functions, different **RandomNumberGenerator** instances can use
different seeds.
