# C# API differences to GDScript

This is a (incomplete) list of API differences between C# and GDScript.

## General differences

As explained in `doc_c_sharp_general_differences`, `PascalCase` is used
to access Godot APIs in C# instead of the `snake_case` used by GDScript
and C++. Where possible, fields and getters/setters have been converted
to properties. In general, the C# Godot API strives to be as idiomatic
as is reasonably possible. See the `doc_c_sharp_styleguide`, which we
encourage you to also use for your own C# code.

In GDScript, the setters/getters of a property can be called directly,
although this is not encouraged. In C#, only the property is defined.
For example, to translate the GDScript code `x.set_name("Friend")` to
C#, write `x.Name = "Friend";`.

A C# IDE will provide intellisense, which is extremely useful when
figuring out renamed C# APIs. The built-in Godot script editor has no
support for C# intellisense, and it also doesn't provide many other C#
development tools that are considered essential. See
`doc_c_sharp_setup_external_editor`.

## Global scope

Global functions and some constants had to be moved to classes, since C#
does not allow declaring them in namespaces. Most global constants were
moved to their own enums.

### Constants

In C#, only primitive types can be constant. For example, the `TAU`
constant is replaced by the `Mathf.Tau` constant, but the
`Vector2.RIGHT` constant is replaced by the `Vector2.Right` read-only
property. This behaves similarly to a constant, but can't be used in
some contexts like `switch` statements.

Global enum constants were moved to their own enums. For example,
`ERR_*` constants were moved to the `Error` enum.

Special cases:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>TYPE_*</code></td>
<td><code>Variant.Type</code> enum</td>
</tr>
<tr>
<td><code>OP_*</code></td>
<td><code>Variant.Operator</code> enum</td>
</tr>
</tbody>
</table>

### Math functions

Math global functions, like `abs`, `acos`, `asin`, `atan` and `atan2`,
are located under `Mathf` as `Abs`, `Acos`, `Asin`, `Atan` and `Atan2`.
The `PI` constant can be found as `Mathf.Pi`.

C# also provides static
[System.Math](https://learn.microsoft.com/en-us/dotnet/api/system.math)
and
[System.MathF](https://learn.microsoft.com/en-us/dotnet/api/system.mathf)
classes that may contain other useful mathematical operations.

### Random functions

Random global functions, like `rand_range` and `rand_seed`, are located
under `GD`. Example: `GD.RandRange` and `GD.RandSeed`.

Consider using
[System.Random](https://learn.microsoft.com/en-us/dotnet/api/system.random)
or, if you need cryptographically strong randomness,
[System.Security.Cryptography.RandomNumberGenerator](https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.randomnumbergenerator).

### Other functions

Many other global functions like `print` and `var_to_str` are located
under `GD`. Example: `GD.Print` and `GD.VarToStr`.

Exceptions:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>weakref(obj)</code></td>
<td><code>GodotObject.WeakRef(obj)</code></td>
</tr>
<tr>
<td><code>instance_from_id(id)</code></td>
<td><code>GodotObject.InstanceFromId(id)</code></td>
</tr>
<tr>
<td><code>is_instance_id_valid(id)</code></td>
<td><code>GodotObject.IsInstanceIdValid(id)</code></td>
</tr>
<tr>
<td><code>is_instance_valid(obj)</code></td>
<td><code>GodotObject.IsInstanceValid(obj)</code></td>
</tr>
</tbody>
</table>

### Tips

Sometimes it can be useful to use the `using static` directive. This
directive allows to access the members and nested types of a class
without specifying the class name.

Example:

    using static Godot.GD;

    public class Test
    {
        static Test()
        {
            Print("Hello"); // Instead of GD.Print("Hello");
        }
    }

### Full list of equivalences

List of Godot's global scope functions and their equivalent in C#:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td>abs</td>
<td>Mathf.Abs</td>
</tr>
<tr>
<td>absf</td>
<td>Mathf.Abs</td>
</tr>
<tr>
<td>absi</td>
<td>Mathf.Abs</td>
</tr>
<tr>
<td>acos</td>
<td>Mathf.Acos</td>
</tr>
<tr>
<td>acosh</td>
<td>Mathf.Acosh</td>
</tr>
<tr>
<td>angle_difference</td>
<td>Mathf.AngleDifference</td>
</tr>
<tr>
<td>asin</td>
<td>Mathf.Asin</td>
</tr>
<tr>
<td>asinh</td>
<td>Mathf.Asinh</td>
</tr>
<tr>
<td>atan</td>
<td>Mathf.Atan</td>
</tr>
<tr>
<td>atan2</td>
<td>Mathf.Atan2</td>
</tr>
<tr>
<td>atanh</td>
<td>Mathf.Atanh</td>
</tr>
<tr>
<td>bezier_derivative</td>
<td>Mathf.BezierDerivative</td>
</tr>
<tr>
<td>bezier_interpolate</td>
<td>Mathf.BezierInterpolate</td>
</tr>
<tr>
<td>bytes_to_var</td>
<td>GD.BytesToVar</td>
</tr>
<tr>
<td>bytes_to_var_with_objects</td>
<td>GD.BytesToVarWithObjects</td>
</tr>
<tr>
<td>ceil</td>
<td>Mathf.Ceil</td>
</tr>
<tr>
<td>ceilf</td>
<td>Mathf.Ceil</td>
</tr>
<tr>
<td>ceili</td>
<td>Mathf.CeilToInt</td>
</tr>
<tr>
<td>clamp</td>
<td>Mathf.Clamp</td>
</tr>
<tr>
<td>clampf</td>
<td>Mathf.Clamp</td>
</tr>
<tr>
<td>clampi</td>
<td>Mathf.Clamp</td>
</tr>
<tr>
<td>cos</td>
<td>Mathf.Cos</td>
</tr>
<tr>
<td>cosh</td>
<td>Mathf.Cosh</td>
</tr>
<tr>
<td>cubic_interpolate</td>
<td>Mathf.CubicInterpolate</td>
</tr>
<tr>
<td>cubic_interpolate_angle</td>
<td>Mathf.CubicInterpolateAngle</td>
</tr>
<tr>
<td>cubic_interpolate_angle_in_time</td>
<td>Mathf.CubicInterpolateInTime</td>
</tr>
<tr>
<td>cubic_interpolate_in_time</td>
<td>Mathf.CubicInterpolateAngleInTime</td>
</tr>
<tr>
<td>db_to_linear</td>
<td>Mathf.DbToLinear</td>
</tr>
<tr>
<td>deg_to_rad</td>
<td>Mathf.DegToRad</td>
</tr>
<tr>
<td>ease</td>
<td>Mathf.Ease</td>
</tr>
<tr>
<td>error_string</td>
<td>Error.ToString</td>
</tr>
<tr>
<td>exp</td>
<td>Mathf.Exp</td>
</tr>
<tr>
<td>floor</td>
<td>Mathf.Floor</td>
</tr>
<tr>
<td>floorf</td>
<td>Mathf.Floor</td>
</tr>
<tr>
<td>floori</td>
<td>Mathf.FloorToInt</td>
</tr>
<tr>
<td>fmod</td>
<td>operator %</td>
</tr>
<tr>
<td>fposmod</td>
<td>Mathf.PosMod</td>
</tr>
<tr>
<td>hash</td>
<td>GD.Hash</td>
</tr>
<tr>
<td>instance_from_id</td>
<td>GodotObject.InstanceFromId</td>
</tr>
<tr>
<td>inverse_lerp</td>
<td>Mathf.InverseLerp</td>
</tr>
<tr>
<td>is_equal_approx</td>
<td>Mathf.IsEqualApprox</td>
</tr>
<tr>
<td>is_finite</td>
<td>Mathf.IsFinite or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.single.isfinite">float.IsFinite</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.double.isfinite">double.IsFinite</a></td>
</tr>
<tr>
<td>is_inf</td>
<td>Mathf.IsInf or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.single.isinfinity">float.IsInfinity</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.double.isinfinity">double.IsInfinity</a></td>
</tr>
<tr>
<td>is_instance_id_valid</td>
<td>GodotObject.IsInstanceIdValid</td>
</tr>
<tr>
<td>is_instance_valid</td>
<td>GodotObject.IsInstanceValid</td>
</tr>
<tr>
<td>is_nan</td>
<td>Mathf.IsNaN or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.single.isnan">float.IsNaN</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.double.isnan">double.IsNaN</a></td>
</tr>
<tr>
<td>is_same</td>
<td>operator == or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.object.referenceequals">object.ReferenceEquals</a></td>
</tr>
<tr>
<td>is_zero_approx</td>
<td>Mathf.IsZeroApprox</td>
</tr>
<tr>
<td>lerp</td>
<td>Mathf.Lerp</td>
</tr>
<tr>
<td>lerp_angle</td>
<td>Mathf.LerpAngle</td>
</tr>
<tr>
<td>lerpf</td>
<td>Mathf.Lerp</td>
</tr>
<tr>
<td>linear_to_db</td>
<td>Mathf.LinearToDb</td>
</tr>
<tr>
<td>log</td>
<td>Mathf.Log</td>
</tr>
<tr>
<td>max</td>
<td>Mathf.Max</td>
</tr>
<tr>
<td>maxf</td>
<td>Mathf.Max</td>
</tr>
<tr>
<td>maxi</td>
<td>Mathf.Max</td>
</tr>
<tr>
<td>min</td>
<td>Mathf.Min</td>
</tr>
<tr>
<td>minf</td>
<td>Mathf.Min</td>
</tr>
<tr>
<td>mini</td>
<td>Mathf.Min</td>
</tr>
<tr>
<td>move_toward</td>
<td>Mathf.MoveToward</td>
</tr>
<tr>
<td>nearest_po2</td>
<td>Mathf.NearestPo2</td>
</tr>
<tr>
<td>pingpong</td>
<td>Mathf.PingPong</td>
</tr>
<tr>
<td>posmod</td>
<td>Mathf.PosMod</td>
</tr>
<tr>
<td>pow</td>
<td>Mathf.Pow</td>
</tr>
<tr>
<td>print</td>
<td>GD.Print</td>
</tr>
<tr>
<td>print_rich</td>
<td>GD.PrintRich</td>
</tr>
<tr>
<td>print_verbose</td>
<td>Use OS.IsStdoutVerbose and GD.Print</td>
</tr>
<tr>
<td>printerr</td>
<td>GD.PrintErr</td>
</tr>
<tr>
<td>printraw</td>
<td>GD.PrintRaw</td>
</tr>
<tr>
<td>prints</td>
<td>GD.PrintS</td>
</tr>
<tr>
<td>printt</td>
<td>GD.PrintT</td>
</tr>
<tr>
<td>push_error</td>
<td>GD.PushError</td>
</tr>
<tr>
<td>push_warning</td>
<td>GD.PushWarning</td>
</tr>
<tr>
<td>rad_to_deg</td>
<td>Mathf.RadToDeg</td>
</tr>
<tr>
<td>rand_from_seed</td>
<td>GD.RandFromSeed</td>
</tr>
<tr>
<td>randf</td>
<td>GD.Randf</td>
</tr>
<tr>
<td>randf_range</td>
<td>GD.RandRange</td>
</tr>
<tr>
<td>randfn</td>
<td>GD.Randfn</td>
</tr>
<tr>
<td>randi</td>
<td>GD.Randi</td>
</tr>
<tr>
<td>randi_range</td>
<td>GD.RandRange</td>
</tr>
<tr>
<td>randomize</td>
<td>GD.Randomize</td>
</tr>
<tr>
<td>remap</td>
<td>Mathf.Remap</td>
</tr>
<tr>
<td>rid_allocate_id</td>
<td>N/A</td>
</tr>
<tr>
<td>rid_from_int64</td>
<td>N/A</td>
</tr>
<tr>
<td>rotate_toward</td>
<td>Mathf.RotateToward</td>
</tr>
<tr>
<td>round</td>
<td>Mathf.Round</td>
</tr>
<tr>
<td>roundf</td>
<td>Mathf.Round</td>
</tr>
<tr>
<td>roundi</td>
<td>Mathf.RoundToInt</td>
</tr>
<tr>
<td>seed</td>
<td>GD.Seed</td>
</tr>
<tr>
<td>sign</td>
<td>Mathf.Sign</td>
</tr>
<tr>
<td>signf</td>
<td>Mathf.Sign</td>
</tr>
<tr>
<td>signi</td>
<td>Mathf.Sign</td>
</tr>
<tr>
<td>sin</td>
<td>Mathf.Sin</td>
</tr>
<tr>
<td>sinh</td>
<td>Mathf.Sinh</td>
</tr>
<tr>
<td>smoothstep</td>
<td>Mathf.SmoothStep</td>
</tr>
<tr>
<td>snapped</td>
<td>Mathf.Snapped</td>
</tr>
<tr>
<td>snappedf</td>
<td>Mathf.Snapped</td>
</tr>
<tr>
<td>snappedi</td>
<td>Mathf.Snapped</td>
</tr>
<tr>
<td>sqrt</td>
<td>Mathf.Sqrt</td>
</tr>
<tr>
<td>step_decimals</td>
<td>Mathf.StepDecimals</td>
</tr>
<tr>
<td>str</td>
<td>Use <a
href="https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated">$
string interpolation</a></td>
</tr>
<tr>
<td>str_to_var</td>
<td>GD.StrToVar</td>
</tr>
<tr>
<td>tan</td>
<td>Mathf.Tan</td>
</tr>
<tr>
<td>tanh</td>
<td>Mathf.Tanh</td>
</tr>
<tr>
<td>type_convert</td>
<td>Variant.As&lt;T&gt; or GD.Convert</td>
</tr>
<tr>
<td>type_string</td>
<td>Variant.Type.ToString</td>
</tr>
<tr>
<td>typeof</td>
<td>Variant.VariantType</td>
</tr>
<tr>
<td>var_to_bytes</td>
<td>GD.VarToBytes</td>
</tr>
<tr>
<td>var_to_bytes_with_objects</td>
<td>GD.VarToBytesWithObjects</td>
</tr>
<tr>
<td>var_to_str</td>
<td>GD.VarToStr</td>
</tr>
<tr>
<td>weakref</td>
<td>GodotObject.WeakRef</td>
</tr>
<tr>
<td>wrap</td>
<td>Mathf.Wrap</td>
</tr>
<tr>
<td>wrapf</td>
<td>Mathf.Wrap</td>
</tr>
<tr>
<td>wrapi</td>
<td>Mathf.Wrap</td>
</tr>
</tbody>
</table>

List of GDScript utility functions and their equivalent in C#:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td>assert</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.diagnostics.debug.assert">System.Diagnostics.Debug.Assert</a></td>
</tr>
<tr>
<td>char</td>
<td>Use explicit conversion: <code>(char)65</code></td>
</tr>
<tr>
<td>convert</td>
<td>GD.Convert</td>
</tr>
<tr>
<td>dict_to_inst</td>
<td>N/A</td>
</tr>
<tr>
<td>get_stack</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.environment.stacktrace">System.Environment.StackTrace</a></td>
</tr>
<tr>
<td>inst_to_dict</td>
<td>N/A</td>
</tr>
<tr>
<td>len</td>
<td>N/A</td>
</tr>
<tr>
<td>load</td>
<td>GD.Load</td>
</tr>
<tr>
<td>preload</td>
<td>N/A</td>
</tr>
<tr>
<td>print_debug</td>
<td>N/A</td>
</tr>
<tr>
<td>print_stack</td>
<td>GD.Print(<a
href="https://learn.microsoft.com/en-us/dotnet/api/system.environment.stacktrace">System.Environment.StackTrace</a>)</td>
</tr>
<tr>
<td>range</td>
<td>GD.Range or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.range">System.Linq.Enumerable.Range</a></td>
</tr>
<tr>
<td>type_exists</td>
<td>ClassDB.ClassExists(type)</td>
</tr>
</tbody>
</table>

`preload`, as it works in GDScript, is not available in C#. Use
`GD.Load` or `ResourceLoader.Load` instead.

## `@export` annotation

Use the `[Export]` attribute instead of the GDScript `@export`
annotation. This attribute can also be provided with optional
`PropertyHint<enum_@GlobalScope_PropertyHint>` and `hintString`
parameters. Default values can be set by assigning a value.

Example:

    using Godot;

    public partial class MyNode : Node
    {
        [Export]
        private NodePath _nodePath;

        [Export]
        private string _name = "default";

        [Export(PropertyHint.Range, "0,100000,1000,or_greater")]
        private int _income;

        [Export(PropertyHint.File, "*.png,*.jpg")]
        private string _icon;
    }

See also: `doc_c_sharp_exports`.

## `signal` keyword

Use the `[Signal]` attribute to declare a signal instead of the GDScript
`signal` keyword. This attribute should be used on a
<span class="title-ref">delegate</span>, whose name signature will be
used to define the signal. The <span class="title-ref">delegate</span>
must have the `EventHandler` suffix, an
<span class="title-ref">event</span> will be generated in the class with
the same name but without the suffix, use that event's name with
`EmitSignal`.

    [Signal]
    delegate void MySignalEventHandler(string willSendAString);

See also: `doc_c_sharp_signals`.

## <span class="title-ref">@onready</span> annotation

GDScript has the ability to defer the initialization of a member
variable until the ready function is called with
<span class="title-ref">@onready</span> (cf.
`doc_gdscript_onready_annotation`). For example:

    @onready var my_label = get_node("MyLabel")

However C# does not have this ability. To achieve the same effect you
need to do this.

    private Label _myLabel;

    public override void _Ready()
    {
        _myLabel = GetNode<Label>("MyLabel");
    }

## Singletons

Singletons are available as static classes rather than using the
singleton pattern. This is to make code less verbose than it would be
with an `Instance` property.

Example:

    Input.IsActionPressed("ui_down")

However, in some very rare cases this is not enough. For example, you
may want to access a member from the base class `GodotObject`, like
`Connect`. For such use cases we provide a static property named
`Singleton` that returns the singleton instance. The type of this
instance is `GodotObject`.

Example:

    Input.Singleton.JoyConnectionChanged += Input_JoyConnectionChanged;

## String

Use `System.String` (`string`). Most of Godot's String methods have an
equivalent in `System.String` or are provided by the `StringExtensions`
class as extension methods.

Example:

    string text = "Get up!";
    string[] bigrams = text.Bigrams(); // ["Ge", "et", "t ", " u", "up", "p!"]

Strings are immutable in .NET, so all methods that manipulate a string
don't modify the original string and return a newly created string with
the modifications applied. To avoid creating multiple string allocations
consider using a
[StringBuilder](https://learn.microsoft.com/en-us/dotnet/api/system.text.stringbuilder).

List of Godot's String methods and their equivalent in C#:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td>begins_with</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.startswith">string.StartsWith</a></td>
</tr>
<tr>
<td>bigrams</td>
<td>StringExtensions.Bigrams</td>
</tr>
<tr>
<td>bin_to_int</td>
<td>StringExtensions.BinToInt</td>
</tr>
<tr>
<td>c_escape</td>
<td>StringExtensions.CEscape</td>
</tr>
<tr>
<td>c_unescape</td>
<td>StringExtensions.CUnescape</td>
</tr>
<tr>
<td>capitalize</td>
<td>StringExtensions.Capitalize</td>
</tr>
<tr>
<td>casecmp_to</td>
<td>StringExtensions.CasecmpTo or StringExtensions.CompareTo (Consider
using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.equals">string.Equals</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.compare">string.Compare</a>)</td>
</tr>
<tr>
<td>chr</td>
<td>N/A</td>
</tr>
<tr>
<td>contains</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.contains">string.Contains</a></td>
</tr>
<tr>
<td>count</td>
<td>StringExtensions.Count (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions">RegEx</a>)</td>
</tr>
<tr>
<td>countn</td>
<td>StringExtensions.CountN (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions">RegEx</a>)</td>
</tr>
<tr>
<td>dedent</td>
<td>StringExtensions.Dedent</td>
</tr>
<tr>
<td>ends_with</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.endswith">string.EndsWith</a></td>
</tr>
<tr>
<td>erase</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.remove">string.Remove</a>
(Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.stringbuilder">StringBuilder</a>
to manipulate strings)</td>
</tr>
<tr>
<td>find</td>
<td>StringExtensions.Find (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.indexof">string.IndexOf</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.indexofany">string.IndexOfAny</a>)</td>
</tr>
<tr>
<td>findn</td>
<td>StringExtensions.FindN (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.indexof">string.IndexOf</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.indexofany">string.IndexOfAny</a>)</td>
</tr>
<tr>
<td>format</td>
<td>Use <a
href="https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated">$
string interpolation</a></td>
</tr>
<tr>
<td>get_base_dir</td>
<td>StringExtensions.GetBaseDir</td>
</tr>
<tr>
<td>get_basename</td>
<td>StringExtensions.GetBaseName</td>
</tr>
<tr>
<td>get_extension</td>
<td>StringExtensions.GetExtension</td>
</tr>
<tr>
<td>get_file</td>
<td>StringExtensions.GetFile</td>
</tr>
<tr>
<td>get_slice</td>
<td>N/A</td>
</tr>
<tr>
<td>get_slice_count</td>
<td>N/A</td>
</tr>
<tr>
<td>get_slicec</td>
<td>N/A</td>
</tr>
<tr>
<td>hash</td>
<td>StringExtensions.Hash (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.object.gethashcode">object.GetHashCode</a>
unless you need to guarantee the same behavior as in GDScript)</td>
</tr>
<tr>
<td>hex_decode</td>
<td>StringExtensions.HexDecode (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.convert.fromhexstring">System.Convert.FromHexString</a>)</td>
</tr>
<tr>
<td>hex_to_int</td>
<td>StringExtensions.HexToInt (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int32.parse">int.Parse</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int64.parse">long.Parse</a>
with <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.globalization.numberstyles#system-globalization-numberstyles-hexnumber">System.Globalization.NumberStyles.HexNumber</a>)</td>
</tr>
<tr>
<td>humanize_size</td>
<td>N/A</td>
</tr>
<tr>
<td>indent</td>
<td>StringExtensions.Indent</td>
</tr>
<tr>
<td>insert</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.insert">string.Insert</a>
(Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.stringbuilder">StringBuilder</a>
to manipulate strings)</td>
</tr>
<tr>
<td>is_absolute_path</td>
<td>StringExtensions.IsAbsolutePath</td>
</tr>
<tr>
<td>is_empty</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.isnullorempty">string.IsNullOrEmpty</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.isnullorwhitespace">string.IsNullOrWhiteSpace</a></td>
</tr>
<tr>
<td>is_relative_path</td>
<td>StringExtensions.IsRelativePath</td>
</tr>
<tr>
<td>is_subsequence_of</td>
<td>StringExtensions.IsSubsequenceOf</td>
</tr>
<tr>
<td>is_subsequence_ofn</td>
<td>StringExtensions.IsSubsequenceOfN</td>
</tr>
<tr>
<td>is_valid_filename</td>
<td>StringExtensions.IsValidFileName</td>
</tr>
<tr>
<td>is_valid_float</td>
<td>StringExtensions.IsValidFloat (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.single.tryparse">float.TryParse</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.double.tryparse">double.TryParse</a>)</td>
</tr>
<tr>
<td>is_valid_hex_number</td>
<td>StringExtensions.IsValidHexNumber</td>
</tr>
<tr>
<td>is_valid_html_color</td>
<td>StringExtensions.IsValidHtmlColor</td>
</tr>
<tr>
<td>is_valid_identifier</td>
<td>StringExtensions.IsValidIdentifier</td>
</tr>
<tr>
<td>is_valid_int</td>
<td>StringExtensions.IsValidInt (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int32.tryparse">int.TryParse</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int64.tryparse">long.TryParse</a>)</td>
</tr>
<tr>
<td>is_valid_ip_address</td>
<td>StringExtensions.IsValidIPAddress</td>
</tr>
<tr>
<td>join</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.join">string.Join</a></td>
</tr>
<tr>
<td>json_escape</td>
<td>StringExtensions.JSONEscape</td>
</tr>
<tr>
<td>left</td>
<td>StringExtensions.Left (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.substring">string.Substring</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.memoryextensions.asspan">string.AsSpan</a>)</td>
</tr>
<tr>
<td>length</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.length">string.Length</a></td>
</tr>
<tr>
<td>lpad</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.padleft">string.PadLeft</a></td>
</tr>
<tr>
<td>lstrip</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.trimstart">string.TrimStart</a></td>
</tr>
<tr>
<td>match</td>
<td>StringExtensions.Match (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions">RegEx</a>)</td>
</tr>
<tr>
<td>matchn</td>
<td>StringExtensions.MatchN (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions">RegEx</a>)</td>
</tr>
<tr>
<td>md5_buffer</td>
<td>StringExtensions.Md5Buffer (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.md5.hashdata">System.Security.Cryptography.MD5.HashData</a>)</td>
</tr>
<tr>
<td>md5_text</td>
<td>StringExtensions.Md5Text (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.md5.hashdata">System.Security.Cryptography.MD5.HashData</a>
with StringExtensions.HexEncode)</td>
</tr>
<tr>
<td>naturalnocasecmp_to</td>
<td>N/A (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.equals">string.Equals</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.compare">string.Compare</a>)</td>
</tr>
<tr>
<td>nocasecmp_to</td>
<td>StringExtensions.NocasecmpTo or StringExtensions.CompareTo (Consider
using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.equals">string.Equals</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.compare">string.Compare</a>)</td>
</tr>
<tr>
<td>num</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.single.tostring">float.ToString</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.double.tostring">double.ToString</a></td>
</tr>
<tr>
<td>num_int64</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int32.tostring">int.ToString</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int64.tostring">long.ToString</a></td>
</tr>
<tr>
<td>num_scientific</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.single.tostring">float.ToString</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.double.tostring">double.ToString</a></td>
</tr>
<tr>
<td>num_uint64</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.uint32.tostring">uint.ToString</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.uint64.tostring">ulong.ToString</a></td>
</tr>
<tr>
<td>pad_decimals</td>
<td>StringExtensions.PadDecimals</td>
</tr>
<tr>
<td>pad_zeros</td>
<td>StringExtensions.PadZeros</td>
</tr>
<tr>
<td>path_join</td>
<td>StringExtensions.PathJoin</td>
</tr>
<tr>
<td>repeat</td>
<td>Use <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.-ctor">string
constructor</a> or a <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.stringbuilder">StringBuilder</a></td>
</tr>
<tr>
<td>replace</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.replace">string.Replace</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions">RegEx</a></td>
</tr>
<tr>
<td>replacen</td>
<td>StringExtensions.ReplaceN (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.replace">string.Replace</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expressions">RegEx</a>)</td>
</tr>
<tr>
<td>reverse</td>
<td>N/A</td>
</tr>
<tr>
<td>rfind</td>
<td>StringExtensions.RFind (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.lastindexof">string.LastIndexOf</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.lastindexofany">string.LastIndexOfAny</a>)</td>
</tr>
<tr>
<td>rfindn</td>
<td>StringExtensions.RFindN (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.lastindexof">string.LastIndexOf</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.lastindexofany">string.LastIndexOfAny</a>)</td>
</tr>
<tr>
<td>right</td>
<td>StringExtensions.Right (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.substring">string.Substring</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.memoryextensions.asspan">string.AsSpan</a>)</td>
</tr>
<tr>
<td>rpad</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.padright">string.PadRight</a></td>
</tr>
<tr>
<td>rsplit</td>
<td>N/A</td>
</tr>
<tr>
<td>rstrip</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.trimend">string.TrimEnd</a></td>
</tr>
<tr>
<td>sha1_buffer</td>
<td>StringExtensions.Sha1Buffer (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.sha1.hashdata">System.Security.Cryptography.SHA1.HashData</a>)</td>
</tr>
<tr>
<td>sha1_text</td>
<td>StringExtensions.Sha1Text (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.sha1.hashdata">System.Security.Cryptography.SHA1.HashData</a>
with StringExtensions.HexEncode)</td>
</tr>
<tr>
<td>sha256_buffer</td>
<td>StringExtensions.Sha256Buffer (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.sha256.hashdata">System.Security.Cryptography.SHA256.HashData</a>)</td>
</tr>
<tr>
<td>sha256_text</td>
<td>StringExtensions.Sha256Text (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.security.cryptography.sha256.hashdata">System.Security.Cryptography.SHA256.HashData</a>
with StringExtensions.HexEncode)</td>
</tr>
<tr>
<td>similarity</td>
<td>StringExtensions.Similarity</td>
</tr>
<tr>
<td>simplify_path</td>
<td>StringExtensions.SimplifyPath</td>
</tr>
<tr>
<td>split</td>
<td>StringExtensions.Split (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.split">string.Split</a>)</td>
</tr>
<tr>
<td>split_floats</td>
<td>StringExtensions.SplitFloat</td>
</tr>
<tr>
<td>strip_edges</td>
<td>StringExtensions.StripEdges (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.trim">string.Trim</a>,
<a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.trimstart">string.TrimStart</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.trimend">string.TrimEnd</a>)</td>
</tr>
<tr>
<td>strip_escapes</td>
<td>StringExtensions.StripEscapes</td>
</tr>
<tr>
<td>substr</td>
<td>StringExtensions.Substr (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.substring">string.Substring</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.memoryextensions.asspan">string.AsSpan</a>)</td>
</tr>
<tr>
<td>to_ascii_buffer</td>
<td>StringExtensions.ToAsciiBuffer (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.asciiencoding.getbytes">System.Text.Encoding.ASCII.GetBytes</a>)</td>
</tr>
<tr>
<td>to_camel_case</td>
<td>StringExtensions.ToCamelCase</td>
</tr>
<tr>
<td>to_float</td>
<td>StringExtensions.ToFloat (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.single.tryparse">float.TryParse</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.double.tryparse">double.TryParse</a>)</td>
</tr>
<tr>
<td>to_int</td>
<td>StringExtensions.ToInt (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int32.tryparse">int.TryParse</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.int64.tryparse">long.TryParse</a>)</td>
</tr>
<tr>
<td>to_lower</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.tolower">string.ToLower</a></td>
</tr>
<tr>
<td>to_pascal_case</td>
<td>StringExtensions.ToPascalCase</td>
</tr>
<tr>
<td>to_snake_case</td>
<td>StringExtensions.ToSnakeCase</td>
</tr>
<tr>
<td>to_upper</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.toupper">string.ToUpper</a></td>
</tr>
<tr>
<td>to_utf16_buffer</td>
<td>StringExtensions.ToUtf16Buffer (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.unicodeencoding.getbytes">System.Text.Encoding.UTF16.GetBytes</a>)</td>
</tr>
<tr>
<td>to_utf32_buffer</td>
<td>StringExtensions.ToUtf32Buffer (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.utf32encoding.getbytes">System.Text.Encoding.UTF32.GetBytes</a>)</td>
</tr>
<tr>
<td>to_utf8_buffer</td>
<td>StringExtensions.ToUtf8Buffer (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.utf8encoding.getbytes">System.Text.Encoding.UTF8.GetBytes</a>)</td>
</tr>
<tr>
<td>to_wchar_buffer</td>
<td>StringExtensions.ToUtf16Buffer in Windows and
StringExtensions.ToUtf32Buffer in other platforms</td>
</tr>
<tr>
<td>trim_prefix</td>
<td>StringExtensions.TrimPrefix</td>
</tr>
<tr>
<td>trim_suffix</td>
<td>StringExtensions.TrimSuffix</td>
</tr>
<tr>
<td>unicode_at</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.string.chars">string[int]</a>
indexer</td>
</tr>
<tr>
<td>uri_decode</td>
<td>StringExtensions.URIDecode (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.uri.unescapedatastring">System.Uri.UnescapeDataString</a>)</td>
</tr>
<tr>
<td>uri_encode</td>
<td>StringExtensions.URIEncode (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.uri.escapedatastring">System.Uri.EscapeDataString</a>)</td>
</tr>
<tr>
<td>validate_node_name</td>
<td>StringExtensions.ValidateNodeName</td>
</tr>
<tr>
<td>xml_escape</td>
<td>StringExtensions.XMLEscape</td>
</tr>
<tr>
<td>xml_unescape</td>
<td>StringExtensions.XMLUnescape</td>
</tr>
</tbody>
</table>

List of Godot's PackedByteArray methods that create a String and their
C# equivalent:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td>get_string_from_ascii</td>
<td>StringExtensions.GetStringFromAscii (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.asciiencoding.getstring">System.Text.Encoding.ASCII.GetString</a>)</td>
</tr>
<tr>
<td>get_string_from_utf16</td>
<td>StringExtensions.GetStringFromUtf16 (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.unicodeencoding.getstring">System.Text.Encoding.UTF16.GetString</a>)</td>
</tr>
<tr>
<td>get_string_from_utf32</td>
<td>StringExtensions.GetStringFromUtf32 (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.utf32encoding.getstring">System.Text.Encoding.UTF32.GetString</a>)</td>
</tr>
<tr>
<td>get_string_from_utf8</td>
<td>StringExtensions.GetStringFromUtf8 (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.text.utf8encoding.getstring">System.Text.Encoding.UTF8.GetString</a>)</td>
</tr>
<tr>
<td>hex_encode</td>
<td>StringExtensions.HexEncode (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.convert.tohexstring">System.Convert.ToHexString</a>)</td>
</tr>
</tbody>
</table>

Note

.NET provides path utility methods under the
[System.IO.Path](https://learn.microsoft.com/en-us/dotnet/api/system.io.path)
class. They can only be used with native OS paths, not Godot paths
(paths that start with `res://` or `user://`). See `doc_data_paths`.

## NodePath

The following method was converted to a property with a different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>is_empty()</code></td>
<td><code>IsEmpty</code></td>
</tr>
</tbody>
</table>

## Signal

The following methods were converted to properties with their respective
names changed:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_name()</code></td>
<td><code>Name</code></td>
</tr>
<tr>
<td><code>get_object()</code></td>
<td><code>Owner</code></td>
</tr>
</tbody>
</table>

The `Signal` type implements the awaitable pattern which means it can be
used with the `await` keyword. See `doc_c_sharp_differences_await`.

Instead of using the `Signal` type, the recommended way to use Godot
signals in C# is to use the generated C# events. See
`doc_c_sharp_signals`.

## Callable

The following methods were converted to properties with their respective
names changed:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_object()</code></td>
<td><code>Target</code></td>
</tr>
<tr>
<td><code>get_method()</code></td>
<td><code>Method</code></td>
</tr>
</tbody>
</table>

Currently C# supports `Callable` if one of the following holds:

-   `Callable` was created using the C# `Callable` type.
-   `Callable` is a basic version of the engine's `Callable`. Custom
    `Callable`s are unsupported. A `Callable` is custom when any of the
    following holds:
    -   `Callable` has bound information (`Callable`s created with
        `bind`/`unbind` are unsupported).
    -   `Callable` was created from other languages through the
        GDExtension API.

Some methods such as `bind` and `unbind` are not implemented, use
lambdas instead:

    string name = "John Doe";
    Callable callable = Callable.From(() => SayHello(name));

    void SayHello(string name)
    {
        GD.Print($"Hello {name}");
    }

The lambda captures the `name` variable so it can be bound to the
`SayHello` method.

## RID

This type is named `Rid` in C# to follow the .NET naming convention.

The following methods were converted to properties with their respective
names changed:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_id()</code></td>
<td><code>Id</code></td>
</tr>
<tr>
<td><code>is_valid()</code></td>
<td><code>IsValid</code></td>
</tr>
</tbody>
</table>

## Basis

Structs cannot have parameterless constructors in C#. Therefore,
`new Basis()` initializes all primitive members to their default value.
Use `Basis.Identity` for the equivalent of `Basis()` in GDScript and
C++.

The following method was converted to a property with a different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_scale()</code></td>
<td><code>Scale</code></td>
</tr>
</tbody>
</table>

## Transform2D

Structs cannot have parameterless constructors in C#. Therefore,
`new Transform2D()` initializes all primitive members to their default
value. Please use `Transform2D.Identity` for the equivalent of
`Transform2D()` in GDScript and C++.

The following methods were converted to properties with their respective
names changed:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_rotation()</code></td>
<td><code>Rotation</code></td>
</tr>
<tr>
<td><code>get_scale()</code></td>
<td><code>Scale</code></td>
</tr>
<tr>
<td><code>get_skew()</code></td>
<td><code>Skew</code></td>
</tr>
</tbody>
</table>

## Transform3D

Structs cannot have parameterless constructors in C#. Therefore,
`new Transform3D()` initializes all primitive members to their default
value. Please use `Transform3D.Identity` for the equivalent of
`Transform3D()` in GDScript and C++.

The following methods were converted to properties with their respective
names changed:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_rotation()</code></td>
<td><code>Rotation</code></td>
</tr>
<tr>
<td><code>get_scale()</code></td>
<td><code>Scale</code></td>
</tr>
</tbody>
</table>

## Rect2

The following field was converted to a property with a *slightly*
different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>end</code></td>
<td><code>End</code></td>
</tr>
</tbody>
</table>

The following method was converted to a property with a different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_area()</code></td>
<td><code>Area</code></td>
</tr>
</tbody>
</table>

## Rect2i

This type is named `Rect2I` in C# to follow the .NET naming convention.

The following field was converted to a property with a *slightly*
different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>end</code></td>
<td><code>End</code></td>
</tr>
</tbody>
</table>

The following method was converted to a property with a different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_area()</code></td>
<td><code>Area</code></td>
</tr>
</tbody>
</table>

## AABB

This type is named `Aabb` in C# to follow the .NET naming convention.

The following method was converted to a property with a different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_volume()</code></td>
<td><code>Volume</code></td>
</tr>
</tbody>
</table>

## Quaternion

Structs cannot have parameterless constructors in C#. Therefore,
`new Quaternion()` initializes all primitive members to their default
value. Please use `Quaternion.Identity` for the equivalent of
`Quaternion()` in GDScript and C++.

## Projection

Structs cannot have parameterless constructors in C#. Therefore,
`new Projection()` initializes all primitive members to their default
value. Please use `Projection.Identity` for the equivalent of
`Projection()` in GDScript and C++.

## Color

Structs cannot have parameterless constructors in C#. Therefore,
`new Color()` initializes all primitive members to their default value
(which represents the transparent black color). Please use
`Colors.Black` for the equivalent of `Color()` in GDScript and C++.

The global `Color8` method to construct a Color from bytes is available
as a static method in the Color type.

The Color constants are available in the `Colors` static class as
readonly properties.

The following method was converted to a property with a different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>get_luminance()</code></td>
<td><code>Luminance</code></td>
</tr>
</tbody>
</table>

The following method was converted to a method with a different name:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>html(String)</code></td>
<td><code>FromHtml(ReadOnlySpan&lt;char&gt;)</code></td>
</tr>
</tbody>
</table>

The following methods are available as constructors:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>hex(int)</code></td>
<td><code>Color(uint)</code></td>
</tr>
<tr>
<td><code>hex64(int)</code></td>
<td><code>Color(ulong)</code></td>
</tr>
</tbody>
</table>

## Array

The equivalent of packed arrays are `System.Array`.

See also `PackedArray in C# <doc_c_sharp_collections_packedarray>`.

Use `Godot.Collections.Array` for an untyped `Variant` array.
`Godot.Collections.Array<T>` is a type-safe wrapper around
`Godot.Collections.Array`.

See also `Array in C# <doc_c_sharp_collections_array>`.

## Dictionary

Use `Godot.Collections.Dictionary` for an untyped `Variant` dictionary.
`Godot.Collections.Dictionary<TKey, TValue>` is a type-safe wrapper
around `Godot.Collections.Dictionary`.

See also `Dictionary in C# <doc_c_sharp_collections_dictionary>`.

## Variant

`Godot.Variant` is used to represent Godot's native
`Variant <class_Variant>` type. Any
`Variant-compatible type <c_sharp_variant_compatible_types>` can be
converted from/to it.

See also: `doc_c_sharp_variant`.

## Communicating with other scripting languages

This is explained extensively in `doc_cross_language_scripting`.

## `await` keyword

Something similar to GDScript's `await` keyword can be achieved with
C#'s [await
keyword](https://docs.microsoft.com/en-US/dotnet/csharp/language-reference/keywords/await).

The `await` keyword in C# can be used with any awaitable expression.
It's commonly used with operands of the types
[Task](https://learn.microsoft.com/en-us/dotnet/api/system.threading.tasks.task),
[Task](TResult),
[ValueTask](https://learn.microsoft.com/en-us/dotnet/api/system.threading.tasks.valuetask),
or [ValueTask](TResult).

An expression `t` is awaitable if one of the following holds:

-   `t` is of compile-time type `dynamic`.
-   `t` has an accessible instance or extension method called
    `GetAwaiter` with no parameters and no type parameters, and a return
    type `A` for which all of the following hold:
    -   `A` implements the interface
        `System.Runtime.CompilerServices.INotifyCompletion`.
    -   `A` has an accessible, readable instance property `IsCompleted`
        of type `bool`.
    -   `A` has an accessible instance method `GetResult` with no
        parameters and no type parameters.

An equivalent of awaiting a signal in GDScript can be achieved with the
`await` keyword and `GodotObject.ToSignal`.

Example:

    public async Task SomeFunction()
    {
        await ToSignal(timer, Timer.SignalName.Timeout);
        GD.Print("After timeout");
    }
