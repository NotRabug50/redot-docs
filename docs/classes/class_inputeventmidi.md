github\_url  
hide

# InputEventMIDI

**Inherits:** `InputEvent<class_InputEvent>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Represents a MIDI message from a MIDI device, such as a musical
keyboard.

classref-introduction-group

## Description

InputEventMIDI stores information about messages from
[MIDI](https://en.wikipedia.org/wiki/MIDI) (Musical Instrument Digital
Interface) devices. These may include musical keyboards, synthesizers,
and drum machines.

MIDI messages can be received over a 5-pin MIDI connector or over USB.
If your device supports both be sure to check the settings in the device
to see which output it is using.

By default, Godot does not detect MIDI devices. You need to call
`OS.open_midi_inputs<class_OS_method_open_midi_inputs>`, first. You can
check which devices are detected with
`OS.get_connected_midi_inputs<class_OS_method_get_connected_midi_inputs>`,
and close the connection with
`OS.close_midi_inputs<class_OS_method_close_midi_inputs>`.

gdscript

func \_ready():  
OS.open\_midi\_inputs() print(OS.get\_connected\_midi\_inputs())

func \_input(input\_event):  
if input\_event is InputEventMIDI:  
\_print\_midi\_info(input\_event)

func \_print\_midi\_info(midi\_event):  
print(midi\_event) print("Channel ", midi\_event.channel) print("Message
", midi\_event.message) print("Pitch ", midi\_event.pitch)
print("Velocity ", midi\_event.velocity) print("Instrument ",
midi\_event.instrument) print("Pressure ", midi\_event.pressure)
print("Controller number: ", midi\_event.controller\_number)
print("Controller value: ", midi\_event.controller\_value)

csharp

public override void \_Ready() { OS.OpenMidiInputs();
GD.Print(OS.GetConnectedMidiInputs()); }

public override void \_Input(InputEvent inputEvent) { if (inputEvent is
InputEventMidi midiEvent) { PrintMIDIInfo(midiEvent); } }

private void PrintMIDIInfo(InputEventMidi midiEvent) {
GD.Print(midiEvent); GD.Print($"Channel {midiEvent.Channel}");
GD.Print($"Message {midiEvent.Message}"); GD.Print($"Pitch
{midiEvent.Pitch}"); GD.Print($"Velocity {midiEvent.Velocity}");
GD.Print($"Instrument {midiEvent.Instrument}"); GD.Print($"Pressure
{midiEvent.Pressure}"); GD.Print($"Controller number:
{midiEvent.ControllerNumber}"); GD.Print($"Controller value:
{midiEvent.ControllerValue}"); }

\*\*Note:\*\* Godot does not support MIDI output, so there is no way to
emit MIDI messages from Godot. Only MIDI input is supported.

classref-introduction-group

## Tutorials

-   [MIDI Message Status Byte
    List](https://www.midi.org/specifications-old/item/table-2-expanded-messages-list-status-bytes)
-   [Wikipedia General MIDI Instrument
    List](https://en.wikipedia.org/wiki/General_MIDI#Program_change_events)
-   [Wikipedia Piano Key Frequencies
    List](https://en.wikipedia.org/wiki/Piano_key_frequencies#List)

classref-reftable-group

## Properties

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **channel** = `0`
`🔗<class_InputEventMIDI_property_channel>`

classref-property-setget

-   `void (No return value.)` **set\_channel**(value: `int<class_int>`)
-   `int<class_int>` **get\_channel**()

The MIDI channel of this message, ranging from `0` to `15`. MIDI channel
`9` is reserved for percussion instruments.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **controller\_number** = `0`
`🔗<class_InputEventMIDI_property_controller_number>`

classref-property-setget

-   `void (No return value.)` **set\_controller\_number**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_controller\_number**()

The unique number of the controller, if
`message<class_InputEventMIDI_property_message>` is
`@GlobalScope.MIDI_MESSAGE_CONTROL_CHANGE<class_@GlobalScope_constant_MIDI_MESSAGE_CONTROL_CHANGE>`,
otherwise this is `0`. This value can be used to identify sliders for
volume, balance, and panning, as well as switches and pedals on the MIDI
device. See the [General MIDI
specification](https://en.wikipedia.org/wiki/General_MIDI#Controller_events)
for a small list.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **controller\_value** = `0`
`🔗<class_InputEventMIDI_property_controller_value>`

classref-property-setget

-   `void (No return value.)` **set\_controller\_value**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_controller\_value**()

The value applied to the controller. If
`message<class_InputEventMIDI_property_message>` is
`@GlobalScope.MIDI_MESSAGE_CONTROL_CHANGE<class_@GlobalScope_constant_MIDI_MESSAGE_CONTROL_CHANGE>`,
this value ranges from `0` to `127`, otherwise it is `0`. See also
`controller_value<class_InputEventMIDI_property_controller_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **instrument** = `0`
`🔗<class_InputEventMIDI_property_instrument>`

classref-property-setget

-   `void (No return value.)` **set\_instrument**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_instrument**()

The instrument (also called *program* or *preset*) used on this MIDI
message. This value ranges from `0` to `127`.

To see what each value means, refer to the [General MIDI's instrument
list](https://en.wikipedia.org/wiki/General_MIDI#Program_change_events).
Keep in mind that the list is off by 1 because it does not begin from 0.
A value of `0` corresponds to the acoustic grand piano.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MIDIMessage<enum_@GlobalScope_MIDIMessage>` **message** = `0`
`🔗<class_InputEventMIDI_property_message>`

classref-property-setget

-   `void (No return value.)` **set\_message**(value:
    `MIDIMessage<enum_@GlobalScope_MIDIMessage>`)
-   `MIDIMessage<enum_@GlobalScope_MIDIMessage>` **get\_message**()

Represents the type of MIDI message (see the
`MIDIMessage<enum_@GlobalScope_MIDIMessage>` enum).

For more information, see the [MIDI message status byte list
chart](https://www.midi.org/specifications-old/item/table-2-expanded-messages-list-status-bytes).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **pitch** = `0`
`🔗<class_InputEventMIDI_property_pitch>`

classref-property-setget

-   `void (No return value.)` **set\_pitch**(value: `int<class_int>`)
-   `int<class_int>` **get\_pitch**()

The pitch index number of this MIDI message. This value ranges from `0`
to `127`.

On a piano, the **middle C** is `60`, followed by a **C-sharp** (`61`),
then a **D** (`62`), and so on. Each octave is split in offsets of 12.
See the "MIDI note number" column of the [piano key frequency
chart](https://en.wikipedia.org/wiki/Piano_key_frequencies) a full list.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **pressure** = `0`
`🔗<class_InputEventMIDI_property_pressure>`

classref-property-setget

-   `void (No return value.)` **set\_pressure**(value: `int<class_int>`)
-   `int<class_int>` **get\_pressure**()

The strength of the key being pressed. This value ranges from `0` to
`127`.

\*\*Note:\*\* For many devices, this value is always `0`. Other devices
such as musical keyboards may simulate pressure by changing the
`velocity<class_InputEventMIDI_property_velocity>`, instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **velocity** = `0`
`🔗<class_InputEventMIDI_property_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_velocity**(value: `int<class_int>`)
-   `int<class_int>` **get\_velocity**()

The velocity of the MIDI message. This value ranges from `0` to `127`.
For a musical keyboard, this corresponds to how quickly the key was
pressed, and is rarely above `110` in practice.

\*\*Note:\*\* Some MIDI devices may send a
`@GlobalScope.MIDI_MESSAGE_NOTE_ON<class_@GlobalScope_constant_MIDI_MESSAGE_NOTE_ON>`
message with `0` velocity and expect it to be treated the same as a
`@GlobalScope.MIDI_MESSAGE_NOTE_OFF<class_@GlobalScope_constant_MIDI_MESSAGE_NOTE_OFF>`
message. If necessary, this can be handled with a few lines of code:

    func _input(event):
        if event is InputEventMIDI:
            if event.message == MIDI_MESSAGE_NOTE_ON and event.velocity > 0:
                print("Note pressed!")
