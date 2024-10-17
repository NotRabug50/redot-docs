github\_url  
hide

# TextServerFallback

**Inherits:** `TextServerExtension<class_TextServerExtension>` **&lt;**
`TextServer<class_TextServer>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A fallback implementation of Godot's text server, without support for
BiDi and complex text layout.

classref-introduction-group

## Description

A fallback implementation of Godot's text server. This fallback is
faster than `TextServerAdvanced<class_TextServerAdvanced>` for
processing a lot of text, but it does not support BiDi and complex text
layout.

\*\*Note:\*\* This text server is not part of official Godot binaries.
If you want to use it, compile the engine with the option
`module_text_server_fb_enabled=yes`.
