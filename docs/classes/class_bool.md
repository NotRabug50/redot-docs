github\_url  
hide

# bool

A built-in boolean type.

classref-introduction-group

## Description

The **bool** is a built-in `Variant<class_Variant>` type that may only
store one of two values: `true` or `false`. You can imagine it as a
switch that can be either turned on or off, or as a binary digit that
can either be 1 or 0.

Booleans can be directly used in `if`, and other conditional statements:

gdscript

var can\_shoot = true if can\_shoot: launch\_bullet()

csharp

bool canShoot = true; if (canShoot) { LaunchBullet(); }

All comparison operators return booleans (`==`, `>`, `<=`, etc.). As
such, it is not necessary to compare booleans themselves. You do not
need to add `== true` or `== false`.

Booleans can be combined with the logical operators `and`, `or`, `not`
to create complex conditions:

gdscript

if bullets &gt; 0 and not is\_reloading():  
launch\_bullet()

if bullets == 0 or is\_reloading():  
play\_clack\_sound()

csharp

if (bullets &gt; 0 && !IsReloading()) { LaunchBullet(); }

if (bullets == 0 || IsReloading()) { PlayClackSound(); }

\*\*Note:\*\* In modern programming languages, logical operators are
evaluated in order. All remaining conditions are skipped if their result
would have no effect on the final value. This concept is known as
[short-circuit
evaluation](https://en.wikipedia.org/wiki/Short-circuit_evaluation) and
can be useful to avoid evaluating expensive conditions in some
performance-critical cases.

\*\*Note:\*\* By convention, built-in methods and properties that return
booleans are usually defined as yes-no questions, single adjectives, or
similar (`String.is_empty<class_String_method_is_empty>`,
`Node.can_process<class_Node_method_can_process>`,
`Camera2D.enabled<class_Camera2D_property_enabled>`, etc.).

classref-reftable-group

## Constructors

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
</tbody>
</table>

classref-reftable-group

## Operators

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constructor Descriptions

classref-constructor

`bool<class_bool>` **bool**() `🔗<class_bool_constructor_bool>`

Constructs a **bool** set to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`bool<class_bool>` **bool**(from: `bool<class_bool>`)

Constructs a **bool** as a copy of the given **bool**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`bool<class_bool>` **bool**(from: `float<class_float>`)

Cast a `float<class_float>` value to a boolean value. Returns `false` if
`from` is equal to `0.0` (including `-0.0`), and `true` for all other
values (including `@GDScript.INF<class_@GDScript_constant_INF>` and
`@GDScript.NAN<class_@GDScript_constant_NAN>`).

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`bool<class_bool>` **bool**(from: `int<class_int>`)

Cast an `int<class_int>` value to a boolean value. Returns `false` if
`from` is equal to `0`, and `true` for all other values.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right: `bool<class_bool>`)
`🔗<class_bool_operator_neq_bool>`

Returns `true` if the two booleans are not equal. That is, one is `true`
and the other is `false`. This operation can be seen as a logical XOR.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;**(right: `bool<class_bool>`)
`🔗<class_bool_operator_lt_bool>`

Returns `true` if the left operand is `false` and the right operand is
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right: `bool<class_bool>`)
`🔗<class_bool_operator_eq_bool>`

Returns `true` if the two booleans are equal. That is, both are `true`
or both are `false`. This operation can be seen as a logical EQ or XNOR.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;**(right: `bool<class_bool>`)
`🔗<class_bool_operator_gt_bool>`

Returns `true` if the left operand is `true` and the right operand is
`false`.
