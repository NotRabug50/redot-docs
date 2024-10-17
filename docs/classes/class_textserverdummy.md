github\_url  
hide

# TextServerDummy

**Inherits:** `TextServerExtension<class_TextServerExtension>` **&lt;**
`TextServer<class_TextServer>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A dummy text server that can't render text or manage fonts.

classref-introduction-group

## Description

A dummy `TextServer<class_TextServer>` interface that doesn't do
anything. Useful for freeing up memory when rendering text is not
needed, as text servers are resource-intensive. It can also be used for
performance comparisons in complex GUIs to check the impact of text
rendering.

A dummy text server is always available at the start of a project.
Here's how to access it:

    var dummy_text_server = TextServerManager.find_interface("Dummy")
    if dummy_text_server != null:
        TextServerManager.set_primary_interface(dummy_text_server)
        # If the other text servers are unneeded, they can be removed:
        for i in TextServerManager.get_interface_count():
            var text_server = TextServerManager.get_interface(i)
            if text_server != dummy_text_server:
                TextServerManager.remove_interface(text_server)

The command line argument `--text-driver Dummy` (case-sensitive) can be
used to force the "Dummy" `TextServer<class_TextServer>` on any project.
