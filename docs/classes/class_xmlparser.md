github\_url  
hide

# XMLParser

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides a low-level interface for creating parsers for XML files.

classref-introduction-group

## Description

Provides a low-level interface for creating parsers for
[XML](https://en.wikipedia.org/wiki/XML) files. This class can serve as
base to make custom XML parsers.

To parse XML, you must open a file with the
`open<class_XMLParser_method_open>` method or a buffer with the
`open_buffer<class_XMLParser_method_open_buffer>` method. Then, the
`read<class_XMLParser_method_read>` method must be called to parse the
next nodes. Most of the methods take into consideration the currently
parsed node.

Here is an example of using **XMLParser** to parse an SVG file (which is
based on XML), printing each element and its attributes as a dictionary:

gdscript

var parser = XMLParser.new() parser.open("path/to/file.svg") while
parser.read() != ERR\_FILE\_EOF: if parser.get\_node\_type() ==
XMLParser.NODE\_ELEMENT: var node\_name = parser.get\_node\_name() var
attributes\_dict = {} for idx in range(parser.get\_attribute\_count()):
attributes\_dict\[parser.get\_attribute\_name(idx)\] =
parser.get\_attribute\_value(idx) print("The ", node\_name, " element
has the following attributes: ", attributes\_dict)

csharp

var parser = new XmlParser(); parser.Open("path/to/file.svg"); while
(parser.Read() != Error.FileEof) { if (parser.GetNodeType() ==
XmlParser.NodeType.Element) { var nodeName = parser.GetNodeName(); var
attributesDict = new Godot.Collections.Dictionary(); for (int idx = 0;
idx &lt; parser.GetAttributeCount(); idx++) {
attributesDict\[parser.GetAttributeName(idx)\] =
parser.GetAttributeValue(idx); } GD.Print($"The {nodeName} element has
the following attributes: {attributesDict}"); } }

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

## Enumerations

classref-enumeration

enum **NodeType**: `🔗<enum_XMLParser_NodeType>`

classref-enumeration-constant

`NodeType<enum_XMLParser_NodeType>` **NODE\_NONE** = `0`

There's no node (no file or buffer opened).

classref-enumeration-constant

`NodeType<enum_XMLParser_NodeType>` **NODE\_ELEMENT** = `1`

An element node type, also known as a tag, e.g. `<title>`.

classref-enumeration-constant

`NodeType<enum_XMLParser_NodeType>` **NODE\_ELEMENT\_END** = `2`

An end of element node type, e.g. `</title>`.

classref-enumeration-constant

`NodeType<enum_XMLParser_NodeType>` **NODE\_TEXT** = `3`

A text node type, i.e. text that is not inside an element. This includes
whitespace.

classref-enumeration-constant

`NodeType<enum_XMLParser_NodeType>` **NODE\_COMMENT** = `4`

A comment node type, e.g. `<!--A comment-->`.

classref-enumeration-constant

`NodeType<enum_XMLParser_NodeType>` **NODE\_CDATA** = `5`

A node type for CDATA (Character Data) sections, e.g.
`<![CDATA[CDATA section]]>`.

classref-enumeration-constant

`NodeType<enum_XMLParser_NodeType>` **NODE\_UNKNOWN** = `6`

An unknown node type.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_attribute\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_attribute_count>`

Returns the number of attributes in the currently parsed element.

\*\*Note:\*\* If this method is used while the currently parsed node is
not `NODE_ELEMENT<class_XMLParser_constant_NODE_ELEMENT>` or
`NODE_ELEMENT_END<class_XMLParser_constant_NODE_ELEMENT_END>`, this
count will not be updated and will still reflect the last element.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_attribute\_name**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_attribute_name>`

Returns the name of an attribute of the currently parsed element,
specified by the `idx` index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_attribute\_value**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_attribute_value>`

Returns the value of an attribute of the currently parsed element,
specified by the `idx` index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_current\_line**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_current_line>`

Returns the current line in the parsed file, counting from 0.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_named\_attribute\_value**(name:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_named_attribute_value>`

Returns the value of an attribute of the currently parsed element,
specified by its `name`. This method will raise an error if the element
has no such attribute.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_named\_attribute\_value\_safe**(name:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_named_attribute_value_safe>`

Returns the value of an attribute of the currently parsed element,
specified by its `name`. This method will return an empty string if the
element has no such attribute.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_node\_data**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_node_data>`

Returns the contents of a text node. This method will raise an error if
the current parsed node is of any other type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_node\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_node_name>`

Returns the name of a node. This method will raise an error if the
currently parsed node is a text node.

\*\*Note:\*\* The content of a
`NODE_CDATA<class_XMLParser_constant_NODE_CDATA>` node and the comment
string of a `NODE_COMMENT<class_XMLParser_constant_NODE_COMMENT>` node
are also considered names.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_node\_offset**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_get_node_offset>`

Returns the byte offset of the currently parsed node since the beginning
of the file or buffer. This is usually equivalent to the number of
characters before the read position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodeType<enum_XMLParser_NodeType>` **get\_node\_type**()
`🔗<class_XMLParser_method_get_node_type>`

Returns the type of the current node. Compare with
`NodeType<enum_XMLParser_NodeType>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_attribute**(name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_has_attribute>`

Returns `true` if the currently parsed element has an attribute with the
`name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_empty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XMLParser_method_is_empty>`

Returns `true` if the currently parsed element is empty, e.g.
`<element />`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **open**(file: `String<class_String>`)
`🔗<class_XMLParser_method_open>`

Opens an XML `file` for parsing. This method returns an error code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **open\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_XMLParser_method_open_buffer>`

Opens an XML raw `buffer` for parsing. This method returns an error
code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **read**()
`🔗<class_XMLParser_method_read>`

Parses the next node in the file. This method returns an error code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **seek**(position: `int<class_int>`)
`🔗<class_XMLParser_method_seek>`

Moves the buffer cursor to a certain offset (since the beginning) and
reads the next node there. This method returns an error code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **skip\_section**()
`🔗<class_XMLParser_method_skip_section>`

Skips the current section. If the currently parsed node contains more
inner nodes, they will be ignored and the cursor will go to the closing
of the current element.
