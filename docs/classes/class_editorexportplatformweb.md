github\_url  
hide

# EditorExportPlatformWeb

**Inherits:** `EditorExportPlatform<class_EditorExportPlatform>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Exporter for the Web.

classref-introduction-group

## Description

The Web exporter customizes how a web build is handled. In the editor's
"Export" window, it is created when adding a new "Web" preset.

\*\*Note:\*\* Godot on Web is rendered inside a `<canvas>` tag.
Normally, the canvas cannot be positioned or resized manually, but
otherwise acts as the main `Window<class_Window>` of the application.

classref-introduction-group

## Tutorials

-   `Exporting for the Web <../tutorials/export/exporting_for_web>`
-   `Web documentation index <../tutorials/platform/web/index>`

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

## Property Descriptions

classref-property

`String<class_String>` **custom\_template/debug**
`🔗<class_EditorExportPlatformWeb_property_custom_template/debug>`

File path to the custom export template used for debug builds. If left
empty, the default template is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_template/release**
`🔗<class_EditorExportPlatformWeb_property_custom_template/release>`

File path to the custom export template used for release builds. If left
empty, the default template is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **html/canvas\_resize\_policy**
`🔗<class_EditorExportPlatformWeb_property_html/canvas_resize_policy>`

Determines how the canvas should be resized by Godot.

-   **None:** The canvas is not automatically resized.
-   **Project:** The size of the canvas is dependent on the
    `ProjectSettings<class_ProjectSettings>`.
-   **Adaptive:** The canvas is automatically resized to fit as much of
    the web page as possible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **html/custom\_html\_shell**
`🔗<class_EditorExportPlatformWeb_property_html/custom_html_shell>`

The custom HTML page that wraps the exported web build. If left empty,
the default HTML shell is used.

For more information, see the
`Customizing HTML5 Shell <../tutorials/platform/web/customizing_html5_shell>`
tutorial.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **html/experimental\_virtual\_keyboard**
`🔗<class_EditorExportPlatformWeb_property_html/experimental_virtual_keyboard>`

**Experimental:** This property may be changed or removed in future
versions.

If `true`, embeds support for a virtual keyboard into the web page,
which is shown when necessary on touchscreen devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **html/export\_icon**
`🔗<class_EditorExportPlatformWeb_property_html/export_icon>`

If `true`, the project icon will be used as the favicon for this
application's web page.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **html/focus\_canvas\_on\_start**
`🔗<class_EditorExportPlatformWeb_property_html/focus_canvas_on_start>`

If `true`, the canvas will be focused as soon as the application is
loaded, if the browser window is already in focus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **html/head\_include**
`🔗<class_EditorExportPlatformWeb_property_html/head_include>`

Additional HTML tags to include inside the `<head>`, such as `<meta>`
tags.

\*\*Note:\*\* You do not need to add a `<title>` tag, as it is
automatically included based on the project's name.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **progressive\_web\_app/background\_color**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/background_color>`

The background color used behind the web application.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **progressive\_web\_app/display**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/display>`

The [display
mode](https://developer.mozilla.org/en-US/docs/Web/Manifest/display/) to
use for this progressive web application. Different browsers and
platforms may not behave the same.

-   **Fullscreen:** Displays the app in fullscreen and hides all of the
    browser's UI elements.
-   **Standalone:** Displays the app in a separate window and hides all
    of the browser's UI elements.
-   **Minimal UI:** Displays the app in a separate window and only shows
    the browser's UI elements for navigation.
-   **Browser:** Displays the app as a normal web page.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **progressive\_web\_app/enabled**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/enabled>`

If `true`, turns this web build into a [progressive web
application](https://en.wikipedia.org/wiki/Progressive_web_app) (PWA).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**progressive\_web\_app/ensure\_cross\_origin\_isolation\_headers**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/ensure_cross_origin_isolation_headers>`

When enabled, the progressive web app will make sure that each request
has cross-origin isolation headers (COEP/COOP).

This can simplify the setup to serve the exported game.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **progressive\_web\_app/icon\_144x144**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/icon_144x144>`

File path to the smallest icon for this web application. If not defined,
defaults to the project icon.

\*\*Note:\*\* If the icon is not 144x144, it will be automatically
resized for the final build.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **progressive\_web\_app/icon\_180x180**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/icon_180x180>`

File path to the small icon for this web application. If not defined,
defaults to the project icon.

\*\*Note:\*\* If the icon is not 180x180, it will be automatically
resized for the final build.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **progressive\_web\_app/icon\_512x512**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/icon_512x512>`

File path to the smallest icon for this web application. If not defined,
defaults to the project icon.

\*\*Note:\*\* If the icon is not 512x512, it will be automatically
resized for the final build.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **progressive\_web\_app/offline\_page**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/offline_page>`

The page to display, should the server hosting the page not be
available. This page is saved in the client's machine.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **progressive\_web\_app/orientation**
`🔗<class_EditorExportPlatformWeb_property_progressive_web_app/orientation>`

The orientation to use when the web application is run through a mobile
device.

-   **Any:** No orientation is forced.
-   **Landscape:** Forces a horizontal layout (wider than it is taller).
-   **Portrait:** Forces a vertical layout (taller than it is wider).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **variant/extensions\_support**
`🔗<class_EditorExportPlatformWeb_property_variant/extensions_support>`

If `true` enables `GDExtension<class_GDExtension>` support for this web
build.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **variant/thread\_support**
`🔗<class_EditorExportPlatformWeb_property_variant/thread_support>`

If `true`, the exported game will support threads. It requires [a
"cross-origin isolated" website](https://web.dev/articles/coop-coep),
which may be difficult to set up and is limited for security reasons
(such as not being able to communicate with third-party websites).

If `false`, the exported game will not support threads. As a result, it
is more prone to performance and audio issues, but will only require to
be run on an HTTPS website.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vram\_texture\_compression/for\_desktop**
`🔗<class_EditorExportPlatformWeb_property_vram_texture_compression/for_desktop>`

If `true`, allows textures to be optimized for desktop through the S3TC
algorithm.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vram\_texture\_compression/for\_mobile**
`🔗<class_EditorExportPlatformWeb_property_vram_texture_compression/for_mobile>`

If `true` allows textures to be optimized for mobile through the ETC2
algorithm.
