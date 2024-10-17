article\_outdated  
True

# HTML5 shell class reference

Projects exported for the Web expose the `Engine` class to the
JavaScript environment, that allows fine control over the engine's
start-up process.

This API is built in an asynchronous manner and requires basic
understanding of
[Promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Using_promises).

## Engine

The `Engine` class provides methods for loading and starting exported
projects on the Web. For default export settings, this is already part
of the exported HTML page. To understand practical use of the `Engine`
class, see
`Custom HTML page for Web export <doc_customizing_html5_shell>`.

### Static Methods

<table>
<colgroup>
<col style="width: 9%" />
<col style="width: 90%" />
</colgroup>
<tbody>
<tr>
<td>Promise</td>
<td><code class="interpreted-text"
role="js:attr">load &lt;Engine.load&gt;</code> <strong>(</strong> string
basePath <strong>)</strong></td>
</tr>
<tr>
<td>void</td>
<td><code class="interpreted-text"
role="js:attr">unload &lt;Engine.unload&gt;</code> <strong>(</strong>
<strong>)</strong></td>
</tr>
<tr>
<td>boolean</td>
<td><code class="interpreted-text"
role="js:attr">isWebGLAvailable &lt;Engine.isWebGLAvailable&gt;</code>
<strong>(</strong> <em>[ number majorVersion=1 ]</em>
<strong>)</strong></td>
</tr>
</tbody>
</table>

### Instance Methods

<table>
<colgroup>
<col style="width: 8%" />
<col style="width: 91%" />
</colgroup>
<tbody>
<tr>
<td>Promise</td>
<td><code class="interpreted-text"
role="js:attr">init &lt;Engine.prototype.init&gt;</code>
<strong>(</strong> <em>[ string basePath ]</em> <strong>)</strong></td>
</tr>
<tr>
<td>Promise</td>
<td><code class="interpreted-text"
role="js:attr">preloadFile &lt;Engine.prototype.preloadFile&gt;</code>
<strong>(</strong> string|ArrayBuffer file <em>[, string path ]</em>
<strong>)</strong></td>
</tr>
<tr>
<td>Promise</td>
<td><code class="interpreted-text"
role="js:attr">start &lt;Engine.prototype.start&gt;</code>
<strong>(</strong> EngineConfig override <strong>)</strong></td>
</tr>
<tr>
<td>Promise</td>
<td><code class="interpreted-text"
role="js:attr">startGame &lt;Engine.prototype.startGame&gt;</code>
<strong>(</strong> EngineConfig override <strong>)</strong></td>
</tr>
<tr>
<td>void</td>
<td><code class="interpreted-text"
role="js:attr">copyToFS &lt;Engine.prototype.copyToFS&gt;</code>
<strong>(</strong> string path, ArrayBuffer buffer
<strong>)</strong></td>
</tr>
<tr>
<td>void</td>
<td><code class="interpreted-text"
role="js:attr">requestQuit &lt;Engine.prototype.requestQuit&gt;</code>
<strong>(</strong> <strong>)</strong></td>
</tr>
</tbody>
</table>

> Create a new Engine instance with the given configuration.
>
> param EngineConfig initConfig  
> The initial config for this instance.
>
> **Static Methods**
>
> > Load the engine from the specified base path.
> >
> > param string basePath  
> > Base path of the engine to load.
> >
> > return  
> > A Promise that resolves once the engine is loaded.
> >
> > rtype  
> > Promise
>
> > Unload the engine to free memory.
> >
> > This method will be called automatically depending on the
> > configuration. See `unloadAfterInit`.
>
> > Check whether WebGL is available. Optionally, specify a particular
> > version of WebGL to check for.
> >
> > param number majorVersion  
> > The major WebGL version to check for.
> >
> > return  
> > If the given major version of WebGL is available.
> >
> > rtype  
> > boolean
>
> **Instance Methods**
>
> > Initialize the engine instance. Optionally, pass the base path to
> > the engine to load it, if it hasn't been loaded yet. See
> > `Engine.load`.
> >
> > param string basePath  
> > Base path of the engine to load.
> >
> > return  
> > A `Promise` that resolves once the engine is loaded and initialized.
> >
> > rtype  
> > Promise
>
> > Load a file so it is available in the instance's file system once it
> > runs. Must be called **before** starting the instance.
> >
> > If not provided, the `path` is derived from the URL of the loaded
> > file.
> >
> > param string|ArrayBuffer file  
> > The file to preload.
> >
> > If a `string` the file will be loaded from that path.
> >
> > If an `ArrayBuffer` or a view on one, the buffer will used as the
> > content of the file.
> >
> > param string path  
> > Path by which the file will be accessible. Required, if `file` is
> > not a string.
> >
> > return  
> > A Promise that resolves once the file is loaded.
> >
> > rtype  
> > Promise
>
> > Start the engine instance using the given override configuration (if
> > any). `startGame <Engine.prototype.startGame>` can be used in
> > typical cases instead.
> >
> > This will initialize the instance if it is not initialized. For
> > manual initialization, see `init <Engine.prototype.init>`. The
> > engine must be loaded beforehand.
> >
> > Fails if a canvas cannot be found on the page, or not specified in
> > the configuration.
> >
> > param EngineConfig override  
> > An optional configuration override.
> >
> > return  
> > Promise that resolves once the engine started.
> >
> > rtype  
> > Promise
>
> > Start the game instance using the given configuration override (if
> > any).
> >
> > This will initialize the instance if it is not initialized. For
> > manual initialization, see `init <Engine.prototype.init>`.
> >
> > This will load the engine if it is not loaded, and preload the main
> > pck.
> >
> > This method expects the initial config (or the override) to have
> > both the `executable` and `mainPack` properties set (normally done
> > by the editor during export).
> >
> > param EngineConfig override  
> > An optional configuration override.
> >
> > return  
> > Promise that resolves once the game started.
> >
> > rtype  
> > Promise
>
> > Create a file at the specified `path` with the passed as `buffer` in
> > the instance's file system.
> >
> > param string path  
> > The location where the file will be created.
> >
> > param ArrayBuffer buffer  
> > The content of the file.
>
> > Request that the current instance quit.
> >
> > This is akin the user pressing the close button in the window
> > manager, and will have no effect if the engine has crashed, or is
> > stuck in a loop.

## Engine configuration

An object used to configure the Engine instance based on godot export
options, and to override those in custom HTML templates if needed.

### Properties

<table style="width:72%;">
<colgroup>
<col style="width: 27%" />
<col style="width: 44%" />
</colgroup>
<tbody>
<tr>
<td>type</td>
<td>name</td>
</tr>
<tr>
<td>boolean</td>
<td><code class="interpreted-text"
role="js:attr">unloadAfterInit</code></td>
</tr>
<tr>
<td>HTMLCanvasElement</td>
<td><code class="interpreted-text" role="js:attr">canvas</code></td>
</tr>
<tr>
<td>string</td>
<td><code class="interpreted-text" role="js:attr">executable</code></td>
</tr>
<tr>
<td>string</td>
<td><code class="interpreted-text" role="js:attr">mainPack</code></td>
</tr>
<tr>
<td>string</td>
<td><code class="interpreted-text" role="js:attr">locale</code></td>
</tr>
<tr>
<td>number</td>
<td><code class="interpreted-text"
role="js:attr">canvasResizePolicy</code></td>
</tr>
<tr>
<td>Array.&lt;string&gt;</td>
<td><code class="interpreted-text" role="js:attr">args</code></td>
</tr>
<tr>
<td>function</td>
<td><code class="interpreted-text" role="js:attr">onExecute</code></td>
</tr>
<tr>
<td>function</td>
<td><code class="interpreted-text" role="js:attr">onExit</code></td>
</tr>
<tr>
<td>function</td>
<td><code class="interpreted-text" role="js:attr">onProgress</code></td>
</tr>
<tr>
<td>function</td>
<td><code class="interpreted-text" role="js:attr">onPrint</code></td>
</tr>
<tr>
<td>function</td>
<td><code class="interpreted-text"
role="js:attr">onPrintError</code></td>
</tr>
</tbody>
</table>

> The Engine configuration object. This is just a typedef, create it
> like a regular object, e.g.:
>
> `const MyConfig = { executable: 'godot', unloadAfterInit: false }`
>
> **Property Descriptions**
>
> > Whether the unload the engine automatically after the instance is
> > initialized.
> >
> > type  
> > boolean
> >
> > value  
> > `true`
>
> > The HTML DOM Canvas object to use.
> >
> > By default, the first canvas element in the document will be used is
> > none is specified.
> >
> > type  
> > HTMLCanvasElement
> >
> > value  
> > `null`
>
> > The name of the WASM file without the extension. (Set by Godot
> > Editor export process).
> >
> > type  
> > string
> >
> > value  
> > `""`
>
> > An alternative name for the game pck to load. The executable name is
> > used otherwise.
> >
> > type  
> > string
> >
> > value  
> > `null`
>
> > Specify a language code to select the proper localization for the
> > game.
> >
> > The browser locale will be used if none is specified. See complete
> > list of `supported locales <doc_locales>`.
> >
> > type  
> > string
> >
> > value  
> > `null`
>
> > The canvas resize policy determines how the canvas should be resized
> > by Godot.
> >
> > `0` means Godot won't do any resizing. This is useful if you want to
> > control the canvas size from javascript code in your template.
> >
> > `1` means Godot will resize the canvas on start, and when changing
> > window size via engine functions.
> >
> > `2` means Godot will adapt the canvas size to match the whole
> > browser window.
> >
> > type  
> > number
> >
> > value  
> > `2`
>
> > The arguments to be passed as command line arguments on startup.
> >
> > See `command line tutorial <doc_command_line_tutorial>`.
> >
> > **Note**: `startGame <Engine.prototype.startGame>` will always add
> > the `--main-pack` argument.
> >
> > type  
> > Array.&lt;string&gt;
> >
> > value  
> > `[]`
>
> > A callback function for handling Godot's `OS.execute` calls.
> >
> > This is for example used in the Web Editor template to switch
> > between Project Manager and editor, and for running the game.
> >
> > param string path  
> > The path that Godot's wants executed.
> >
> > param Array.&lt;string&gt; args  
> > The arguments of the "command" to execute.
>
> > A callback function for being notified when the Godot instance
> > quits.
> >
> > **Note**: This function will not be called if the engine crashes or
> > become unresponsive.
> >
> > param number status\_code  
> > The status code returned by Godot on exit.
>
> > A callback function for displaying download progress.
> >
> > The function is called once per frame while downloading files, so
> > the usage of `requestAnimationFrame()` is not necessary.
> >
> > If the callback function receives a total amount of bytes as 0, this
> > means that it is impossible to calculate. Possible reasons include:
> >
> > -   Files are delivered with server-side chunked compression
> > -   Files are delivered with server-side compression on Chromium
> > -   Not all file downloads have started yet (usually on servers
> >     without multi-threading)
> >
> > param number current  
> > The current amount of downloaded bytes so far.
> >
> > param number total  
> > The total amount of bytes to be downloaded.
>
> > A callback function for handling the standard output stream. This
> > method should usually only be used in debug pages.
> >
> > By default, `console.log()` is used.
> >
> > param \* var\_args  
> > A variadic number of arguments to be printed.
>
> > A callback function for handling the standard error stream. This
> > method should usually only be used in debug pages.
> >
> > By default, `console.error()` is used.
> >
> > param \* var\_args  
> > A variadic number of arguments to be printed as errors.
