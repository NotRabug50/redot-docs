# Runtime file loading and saving

See `doc_saving_games` for information on saving and loading game
progression.

Sometimes, `exporting packs, patches, and mods <doc_exporting_pcks>` is
not ideal when you want players to be able to load user-generated
content in your project. It requires users to generate a PCK or ZIP file
through the Godot editor, which contains resources imported by Godot.

Example use cases for runtime file loading and saving include:

-   Loading texture packs designed for the game.
-   Loading user-provided audio tracks and playing them back in an
    in-game radio station.
-   Loading custom levels or 3D models that can be designed with any 3D
    DCC that can export to glTF (including glTF scenes saved by Godot at
    runtime).
-   Using user-provided fonts for menus and HUD.
-   Saving/loading a file format that can contain multiple files but can
    still easily be read by other applications (ZIP).
-   Loading files created by another game or program, or even game data
    files from another game not made with Godot.

Runtime file loading can be combined with
`HTTP requests <doc_http_request_class>` to load resources from the
Internet directly.

Warning

Do **not** use this runtime loading approach to load resources that are
part of the project, as it's less efficient and doesn't allow benefiting
from Godot's resource handling functionality (such as translation
remaps). See `doc_import_process` for details.

You can see how saving and loading works in action using the [Run-time
File Saving and Loading (Serialization) demo
project](https://github.com/godotengine/godot-demo-projects/blob/master/loading/runtime_save_load).

## Plain text and binary files

Godot's `class_FileAccess` class provides methods to access files on the
filesystem for reading and writing:

.. code-tab:: gdscript

func save\_file(content):  
var file = FileAccess.open("/path/to/file.txt", FileAccess.WRITE)
file.store\_string(content)

func load\_file():  
var file = FileAccess.open("/path/to/file.txt", FileAccess.READ) var
content = file.get\_as\_text() return content

csharp

private void SaveFile(string content) { using var file =
FileAccess.Open("/Path/To/File.txt", FileAccess.ModeFlags.Write);
file.StoreString(content); }

private string LoadFile() { using var file =
FileAccess.Open("/Path/To/File.txt", FileAccess.ModeFlags.Read); string
content = file.GetAsText(); return content; }

To handle custom binary formats (such as loading file formats not
supported by Godot), `class_FileAccess` provides several methods to
read/write integers, floats, strings and more. These FileAccess methods
have names that start with `get_` and `store_`.

If you need more control over reading binary files or need to read
binary streams that are not part of a file, `class_PackedByteArray`
provides several helper methods to decode/encode series of bytes to
integers, floats, strings and more. These PackedByteArray methods have
names that start with `decode_` and `encode_`. See also
`doc_binary_serialization_api`.

## Images

Image's `Image.load_from_file <class_Image_method_load_from_file>`
static method handles everything, from format detection based on file
extension to reading the file from disk.

If you need error handling or more control (such as changing the scale
an SVG is loaded at), use one of the following methods depending on the
file format:

-   `Image.load_jpg_from_buffer <class_Image_method_load_jpg_from_buffer>`
-   `Image.load_ktx_from_buffer <class_Image_method_load_ktx_from_buffer>`
-   `Image.load_png_from_buffer <class_Image_method_load_png_from_buffer>`
-   `Image.load_svg_from_buffer <class_Image_method_load_svg_from_buffer>`
    or
    `Image.load_svg_from_string <class_Image_method_load_svg_from_string>`
-   `Image.load_tga_from_buffer <class_Image_method_load_tga_from_buffer>`
-   `Image.load_webp_from_buffer <class_Image_method_load_webp_from_buffer>`

Several image formats can also be saved by Godot at runtime using the
following methods:

-   `Image.save_png <class_Image_method_save_png>` or
    `Image.save_png_to_buffer <class_Image_method_save_png_to_buffer>`
-   `Image.save_webp <class_Image_method_save_webp>` or
    `Image.save_webp_to_buffer <class_Image_method_save_webp_to_buffer>`
-   `Image.save_jpg <class_Image_method_save_jpg>` or
    `Image.save_jpg_to_buffer <class_Image_method_save_jpg_to_buffer>`
-   `Image.save_exr <class_Image_method_save_exr>` or
    `Image.save_exr_to_buffer <class_Image_method_save_exr_to_buffer>`
    *(only available in editor builds, cannot be used in exported
    projects)*

The methods with the `to_buffer` suffix save the image to a
PackedByteArray instead of the filesystem. This is useful to send the
image over the network or into a ZIP archive without having to write it
on the filesystem. This can increase performance by reducing I/O
utilization.

Note

If displaying the loaded image on a 3D surface, make sure to call
`Image.generate_mipmaps <class_Image_method_generate_mipmaps>` so that
the texture doesn't look grainy when viewed at a distance. This is also
useful in 2D when following instructions on
`reducing aliasing when downsampling <doc_multiple_resolutions_reducing_aliasing_on_downsampling>`.

Example of loading an image and displaying it in a `class_TextureRect`
node (which requires conversion to `class_ImageTexture`):

.. code-tab:: gdscript

\# Load an image of any format supported by Godot from the filesystem.
var image = Image.load\_from\_file(path) \# Optionally, generate mipmaps
if displaying the texture on a 3D surface \# so that the texture doesn't
look grainy when viewed at a distance. \#image.generate\_mipmaps()
$TextureRect.texture = ImageTexture.create\_from\_image(image)

\# Save the loaded Image to a PNG image.
image.save\_png("/path/to/file.png")

\# Save the converted ImageTexture to a PNG image.
$TextureRect.texture.get\_image().save\_png("/path/to/file.png")

csharp

// Load an image of any format supported by Godot from the filesystem.
var image = Image.LoadFromFile(path); // Optionally, generate mipmaps if
displaying the texture on a 3D surface // so that the texture doesn't
look grainy when viewed at a distance. // image.GenerateMipmaps();
GetNode&lt;TextureRect&gt;("TextureRect").Texture =
ImageTexture.CreateFromImage(image);

// Save the loaded Image to a PNG image.
image.SavePng("/Path/To/File.png");

// Save the converted ImageTexture to a PNG image.
GetNode&lt;TextureRect&gt;("TextureRect").Texture.GetImage().SavePng("/Path/To/File.png");

## Audio/video files

Godot supports loading Ogg Vorbis audio at runtime. Note that not *all*
files with an `.ogg` extension may be Ogg Vorbis files. Some may be Ogg
Theora videos, or contain Opus audio within an Ogg container. These
files will **not** load correctly as audio files in Godot.

Example of loading an Ogg Vorbis audio file in an
`class_AudioStreamPlayer` node:

.. code-tab:: gdscript

$AudioStreamPlayer.stream = AudioStreamOggVorbis.load\_from\_file(path)

csharp

GetNode&lt;AudioStreamPlayer&gt;("AudioStreamPlayer").Stream =
AudioStreamOggVorbis.LoadFromFile(path);

Example of loading an Ogg Theora video file in a
`class_VideoStreamPlayer` node:

.. code-tab:: gdscript

var video\_stream\_theora = VideoStreamTheora.new() \# File extension is
ignored, so it is possible to load Ogg Theora videos \# that have an
<span class="title-ref">.ogg</span> extension this way.
video\_stream\_theora.file = "/path/to/file.ogv"
$VideoStreamPlayer.stream = video\_stream\_theora

\# VideoStreamPlayer's Autoplay property won't work if the stream is
empty \# before this property is set, so call
<span class="title-ref">play()</span> after setting
<span class="title-ref">stream</span>. $VideoStreamPlayer.play()

csharp

var videoStreamTheora = new VideoStreamTheora(); // File extension is
ignored, so it is possible to load Ogg Theora videos // that have an
<span class="title-ref">.ogg</span> extension this way.
videoStreamTheora.File = "/Path/To/File.ogv";
GetNode&lt;VideoStreamPlayer&gt;("VideoStreamPlayer").Stream =
videoStreamTheora;

// VideoStreamPlayer's Autoplay property won't work if the stream is
empty // before this property is set, so call
<span class="title-ref">Play()</span> after setting
<span class="title-ref">Stream</span>.
GetNode&lt;VideoStreamPlayer&gt;("VideoStreamPlayer").Play();

Note

Godot doesn't support runtime loading of MP3 or WAV files yet. Until
this is implemented, it's feasible to implement runtime WAV loading
using a script since `class_AudioStreamWAV`'s `data` property is exposed
to scripting.

It's still possible to *save* WAV files using
`AudioStreamWAV.save_to_wav <class_AudioStreamWAV_method_save_to_wav>`,
which is useful for procedurally generated audio or microphone
recordings.

## 3D scenes

Godot has first-class support for glTF 2.0, both in the editor and
exported projects. Using `class_gltfdocument` and `class_gltfstate`
together, Godot can load and save glTF files in exported projects, in
both text (`.gltf`) and binary (`.glb`) formats. The binary format
should be preferred as it's faster to write and smaller, but the text
format is easier to debug.

Example of loading a glTF scene and appending its root node to the
scene:

.. code-tab:: gdscript

\# Load an existing glTF scene. \# GLTFState is used by GLTFDocument to
store the loaded scene's state. \# GLTFDocument is the class that
handles actually loading glTF data into a Godot node tree, \# which
means it supports glTF features such as lights and cameras. var
gltf\_document\_load = GLTFDocument.new() var gltf\_state\_load =
GLTFState.new() var error =
gltf\_document\_load.append\_from\_file("/path/to/file.gltf",
gltf\_state\_load) if error == OK: var gltf\_scene\_root\_node =
gltf\_document\_load.generate\_scene(gltf\_state\_load)
add\_child(gltf\_scene\_root\_node) else: show\_error("Couldn't load
glTF scene (error code: %s)." % error\_string(error))

\# Save a new glTF scene. var gltf\_document\_save := GLTFDocument.new()
var gltf\_state\_save := GLTFState.new()
gltf\_document\_save.append\_from\_scene(gltf\_scene\_root\_node,
gltf\_state\_save) \# The file extension in the output
<span class="title-ref">path</span>
(<span class="title-ref">.gltf</span> or
<span class="title-ref">.glb</span>) determines \# whether the output
uses text or binary format. \#
<span class="title-ref">GLTFDocument.generate\_buffer()</span> is also
available for saving to memory.
gltf\_document\_save.write\_to\_filesystem(gltf\_state\_save, path)

csharp

// Load an existing glTF scene. // GLTFState is used by GLTFDocument to
store the loaded scene's state. // GLTFDocument is the class that
handles actually loading glTF data into a Godot node tree, // which
means it supports glTF features such as lights and cameras. var
gltfDocumentLoad = new GltfDocument(); var gltfStateLoad = new
GltfState(); var error =
gltfDocumentLoad.AppendFromFile("/Path/To/File.gltf", gltfStateLoad); if
(error == Error.Ok) { var gltfSceneRootNode =
gltfDocumentLoad.GenerateScene(gltfStateLoad);
AddChild(gltfSceneRootNode); } else { GD.PrintErr($"Couldn't load glTF
scene (error code: {error})."); }

// Save a new glTF scene. var gltfDocumentSave = new GltfDocument(); var
gltfStateSave = new GltfState();
gltfDocumentSave.AppendFromScene(gltfSceneRootNode, gltfStateSave); //
The file extension in the output <span class="title-ref">path</span>
(<span class="title-ref">.gltf</span> or
<span class="title-ref">.glb</span>) determines // whether the output
uses text or binary format. //
<span class="title-ref">GltfDocument.GenerateBuffer()</span> is also
available for saving to memory.
gltfDocumentSave.WriteToFilesystem(gltfStateSave, path);

Note

When loading a glTF scene, a *base path* must be set so that external
resources like textures can be loaded correctly. When loading from a
file, the base path is automatically set to the folder containing the
file. When loading from a buffer, this base path must be manually set as
there is no way for Godot to infer this path.

To set the base path, set
`GLTFState.base_path <class_GLTFState_property_base_path>` on your
GLTFState instance *before* calling
`GLTFDocument.append_from_buffer <class_GLTFDocument_method_append_from_buffer>`
or
`GLTFDocument.append_from_file <class_GLTFDocument_method_append_from_file>`.

## Fonts

`FontFile.load_dynamic_font <class_FontFile_method_load_bitmap_font>`
supports the following font file formats: TTF, OTF, WOFF, WOFF2, PFB,
PFM

On the other hand,
`FontFile.load_bitmap_font <class_FontFile_method_load_bitmap_font>`
supports the [BMFont](https://www.angelcode.com/products/bmfont/) format
(`.fnt` or `.font`).

Additionally, it is possible to load any font that is installed on the
system using Godot's support for `doc_using_fonts_system_fonts`.

Example of loading a font file automatically according to its file
extension, then adding it as a theme override to a `class_Label` node:

.. code-tab:: gdscript

var path = "/path/to/font.ttf" var path\_lower = path.to\_lower() var
font\_file = FontFile.new() if ( path\_lower.ends\_with(".ttf") or
path\_lower.ends\_with(".otf") or path\_lower.ends\_with(".woff") or
path\_lower.ends\_with(".woff2") or path\_lower.ends\_with(".pfb") or
path\_lower.ends\_with(".pfm") ): font\_file.load\_dynamic\_font(path)
elif path\_lower.ends\_with(".fnt") or path\_lower.ends\_with(".font"):
font\_file.load\_bitmap\_font(path) else: push\_error("Invalid font file
format.")

if not font\_file.data.is\_empty():  
\# If font was loaded successfully, add it as a theme override.
$Label.add\_theme\_font\_override("font", font\_file)

csharp

string path = "/Path/To/Font.ttf"; var fontFile = new FontFile();

if (  
path.EndsWith(".ttf", StringComparison.OrdinalIgnoreCase) ||
path.EndsWith(".otf", StringComparison.OrdinalIgnoreCase) ||
path.EndsWith(".woff", StringComparison.OrdinalIgnoreCase) ||
path.EndsWith(".woff2", StringComparison.OrdinalIgnoreCase) ||
path.EndsWith(".pfb", StringComparison.OrdinalIgnoreCase) ||
path.EndsWith(".pfm", StringComparison.OrdinalIgnoreCase)

### )

> fontFile.LoadDynamicFont(path);

} else if (path.EndsWith(".fnt", StringComparison.OrdinalIgnoreCase) ||
path.EndsWith(".font", StringComparison.OrdinalIgnoreCase)) {
fontFile.LoadBitmapFont(path); } else { GD.PrintErr("Invalid font file
format."); }

if (!fontFile.Data.IsEmpty()) { // If font was loaded successfully, add
it as a theme override.
GetNode&lt;Label&gt;("Label").AddThemeFontOverride("font", fontFile); }

## ZIP archives

Godot supports reading and writing ZIP archives using the
`class_zipreader` and `class_zippacker` classes. This supports any ZIP
file, including files generated by Godot's "Export PCK/ZIP"
functionality (although these will contain imported Godot resources
rather than the original project files).

Note

Use
`ProjectSettings.load_resource_pack <class_ProjectSettings_method_load_resource_pack>`
to load PCK or ZIP files exported by Godot as
`additional data packs <doc_exporting_pcks>`. That approach is preferred
for DLCs, as it makes interacting with additional data packs seamless
(virtual filesystem).

This ZIP archive support can be combined with runtime image, 3D scene
and audio loading to provide a seamless modding experience without
requiring users to go through the Godot editor to generate PCK/ZIP
files.

Example that lists files in a ZIP archive in an `class_ItemList` node,
then writes contents read from it to a new ZIP archive (essentially
duplicating the archive):

.. code-tab:: gdscript

\# Load an existing ZIP archive. var zip\_reader = ZIPReader.new()
zip\_reader.open(path) var files = zip\_reader.get\_files() \# The list
of files isn't sorted by default. Sort it for more consistent
processing. files.sort() for file in files: $ItemList.add\_item(file,
null) \# Make folders disabled in the list.
$ItemList.set\_item\_disabled(-1, file.ends\_with("/"))

\# Save a new ZIP archive. var zip\_packer = ZIPPacker.new() var error =
zip\_packer.open(path) if error != OK: push\_error("Couldn't open path
for saving ZIP archive (error code: %s)." % error\_string(error)) return

\# Reuse the above ZIPReader instance to read files from an existing ZIP
archive. for file in zip\_reader.get\_files():
zip\_packer.start\_file(file)
zip\_packer.write\_file(zip\_reader.read\_file(file))
zip\_packer.close\_file()

zip\_packer.close()

csharp

// Load an existing ZIP archive. var zipReader = new ZipReader();
zipReader.Open(path); string\[\] files = zipReader.GetFiles(); // The
list of files isn't sorted by default. Sort it for more consistent
processing. Array.Sort(files); foreach (string file in files) {
GetNode&lt;ItemList&gt;("ItemList").AddItem(file); // Make folders
disabled in the list.
GetNode&lt;ItemList&gt;("ItemList").SetItemDisabled(-1,
file.EndsWith('/')); }

// Save a new ZIP archive. var zipPacker = new ZipPacker(); var error =
zipPacker.Open(path); if (error != Error.Ok) { GD.PrintErr($"Couldn't
open path for saving ZIP archive (error code: {error})."); return; }

// Reuse the above ZIPReader instance to read files from an existing ZIP
archive. foreach (string file in zipReader.GetFiles()) {
zipPacker.StartFile(file);
zipPacker.WriteFile(zipReader.ReadFile(file)); zipPacker.CloseFile(); }

zipPacker.Close();
