# Exporting for macOS

This page describes how to export a Godot project to macOS. If you're
looking to compile editor or export template binaries from source
instead, read `doc_compiling_for_macos`.

macOS apps exported with the official export templates are exported as a
single "Universal 2" binary `.app` bundle, a folder with a specific
structure which stores the executable, libraries and all the project
files. This bundle can be exported as is, packed in a ZIP archive or DMG
disk image (only supported when exporting from a computer running
macOS). [Universal binaries for macOS support both Intel x86\_64 and
ARM64 (Apple silicon, i.e. M1)
architectures](https://developer.apple.com/documentation/apple-silicon/building-a-universal-macos-binary).

Warning

Due to file system limitations, raw `.app` bundles exported from Windows
lack `executable` flag and won't run on macOS. To fix it, use the
`chmod +x {executable_name}` command after transferring the exported
`.app` to macOS or Linux. Projects exported as `.zip` aren't affected by
this issue. The main executable located in the `Contents/MacOS/`
subfolder, as well as optional helper executables in the
`Contents/Helpers/` subfolder, should have `executable` permission for
the `.app` bundle to be valid.

## Requirements

-   Download the Godot export templates. Use the Godot menu:
    `Editor > Manage Export Templates`.
-   A valid and unique `Bundle identifier` should be set in the
    `Application` section of the export options.

Warning

Projects exported without code signing and notarization will be blocked
by Gatekeeper if they are downloaded from unknown sources, see the
`Running Godot apps on macOS <doc_running_on_macos>` page for more
information.

## Code signing and notarization

By default, macOS will run only applications that are signed and
notarized. If you use any other signing configuration, see
`Running Godot apps on macOS <doc_running_on_macos>` for workarounds.

To notarize an app, you **must** have a valid [Apple Developer ID
Certificate](https://developer.apple.com/).

### If you have an Apple Developer ID Certificate and exporting from macOS

Install [Xcode](https://developer.apple.com/xcode/) command line tools
and open Xcode at least once or run the
`sudo xcodebuild -license accept` command to accept license agreement.

#### To sign exported app

-   Select `Xcode codesign` in the `Code Signing > Codesign` option.
-   Set valid Apple ID certificate identity (certificate "Common Name")
    in the `Code Signing > Identity` section.

#### To notarize exported app

-   Select `Xcode altool` in the `Notarization > Notarization` option.
-   Disable the `Debugging` entitlement.
-   Set valid Apple ID login / app. specific password or [App Store
    Connect](https://developer.apple.com/documentation/appstoreconnectapi)
    API UUID / Key in the `Notarization` section.

You can use the `xcrun notarytool history` command to check notarization
status and use the `xcrun notarytool log {ID}` command to download the
notarization log.

If you encounter notarization issues, see [Resolving common notarization
issues](https://developer.apple.com/documentation/security/notarizing_macos_software_before_distribution/resolving_common_notarization_issues)
for more info.

After notarization is completed, [staple the
ticket](https://developer.apple.com/documentation/security/notarizing_macos_software_before_distribution/customizing_the_notarization_workflow)
to the exported project.

### If you have an Apple Developer ID Certificate and exporting from Linux or Windows

Install [PyOxidizer
rcodesign](https://github.com/indygreg/apple-platform-rs/tree/main/apple-codesign),
and configure the path to `rcodesign` in the
`Editor Settings > Export > macOS > rcodesign`.

#### To sign exported app

-   Select `PyOxidizer rcodesign` in the `Code Signing > Codesign`
    option.
-   Set valid Apple ID PKCS \#12 certificate file and password in the
    `Code Signing` section.

#### To notarize exported app

-   Select `PyOxidizer rcodesign` in the `Notarization > Notarization`
    option.
-   Disable the `Debugging` entitlement.
-   Set valid [App Store
    Connect](https://developer.apple.com/documentation/appstoreconnectapi)
    API UUID / Key in the `Notarization` section.

You can use the `rcodesign notary-log` command to check notarization
status.

After notarization is completed, use the `rcodesign staple` command to
staple the ticket to the exported project.

### If you do not have an Apple Developer ID Certificate

-   Select `Built-in (ad-hoc only)` in the `Code Signing > Codesign`
    option.
-   Select `Disabled` in the `Notarization > Notarization` option.

In this case Godot will use an ad-hoc signature, which will make running
an exported app easier for the end users, see the
`Running Godot apps on macOS <doc_running_on_macos>` page for more
information.

### Signing Options

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr>
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Codesign</td>
<td>Tool to use for code signing.</td>
</tr>
<tr>
<td>Identity</td>
<td>The "Full Name" or "Common Name" of the signing identity, store in
the macOS keychain.<a href="#fn1" class="footnote-ref" id="fnref1"
role="doc-noteref"><sup>1</sup></a></td>
</tr>
<tr>
<td>Certificate File</td>
<td>The PKCS #12 certificate file.<a href="#fn2" class="footnote-ref"
id="fnref2" role="doc-noteref"><sup>2</sup></a></td>
</tr>
<tr>
<td>Certificate Password</td>
<td>Password for the certificate file.<a href="#fn3"
class="footnote-ref" id="fnref3"
role="doc-noteref"><sup>3</sup></a></td>
</tr>
<tr>
<td>Custom Options</td>
<td>Array of command line arguments passed to the code signing
tool.</td>
</tr>
</tbody>
</table>
<section id="footnotes" class="footnotes footnotes-end-of-document"
role="doc-endnotes">
<hr />
<ol>
<li id="fn1"><p>This option is visible only when signing with Xcode
codesign.<a href="#fnref1" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
<li id="fn2"><p>These options are visible only when signing with
PyOxidizer rcodesign.<a href="#fnref2" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
<li id="fn3"><p>These options are visible only when signing with
PyOxidizer rcodesign.<a href="#fnref3" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
</ol>
</section>

### Notarization Options

<table>
<colgroup>
<col style="width: 10%" />
<col style="width: 89%" />
</colgroup>
<thead>
<tr>
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Notarization</td>
<td>Tool to use for notarization.</td>
</tr>
<tr>
<td>Apple ID Name</td>
<td>Apple ID account name (email address).<a href="#fn1"
class="footnote-ref" id="fnref1"
role="doc-noteref"><sup>1</sup></a></td>
</tr>
<tr>
<td>Apple ID Password</td>
<td>Apple ID app-specific password. See <a
href="https://support.apple.com/en-us/HT204397">Using app-specific
passwords</a> to enable two-factor authentication and create app
password.<a href="#fn2" class="footnote-ref" id="fnref2"
role="doc-noteref"><sup>2</sup></a></td>
</tr>
<tr>
<td>Apple Team ID</td>
<td>Team ID ("Organization Unit"), if your Apple ID belongs to multiple
teams (optional).<a href="#fn3" class="footnote-ref" id="fnref3"
role="doc-noteref"><sup>3</sup></a></td>
</tr>
<tr>
<td>API UUID</td>
<td>Apple <a
href="https://developer.apple.com/documentation/appstoreconnectapi">App
Store Connect</a> API issuer UUID.</td>
</tr>
<tr>
<td>API Key</td>
<td>Apple <a
href="https://developer.apple.com/documentation/appstoreconnectapi">App
Store Connect</a> API key.</td>
</tr>
</tbody>
</table>
<section id="footnotes" class="footnotes footnotes-end-of-document"
role="doc-endnotes">
<hr />
<ol>
<li id="fn1"><p>These options are visible only when notarizing with
Xcode altool.<a href="#fnref1" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
<li id="fn2"><p>These options are visible only when notarizing with
Xcode altool.<a href="#fnref2" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
<li id="fn3"><p>These options are visible only when notarizing with
Xcode altool.<a href="#fnref3" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
</ol>
</section>

Note

You should set either Apple ID Name/Password or App Store Connect API
UUID/Key.

See [Notarizing macOS Software Before
Distribution](https://developer.apple.com/documentation/security/notarizing_macos_software_before_distribution?language=objc)
for more info.

## Entitlements

### Hardened Runtime Entitlements

Hardened Runtime entitlements manage security options and resource
access policy. See [Hardened
Runtime](https://developer.apple.com/documentation/security/hardened_runtime?language=objc)
for more info.

<table>
<colgroup>
<col style="width: 17%" />
<col style="width: 82%" />
</colgroup>
<thead>
<tr>
<th>Entitlement</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Allow JIT Code Execution<a href="#fn1" class="footnote-ref"
id="fnref1" role="doc-noteref"><sup>1</sup></a></td>
<td>Allows creating writable and executable memory for JIT code. If you
are using add-ons with dynamic or self-modifying native code, enable
them according to the add-on documentation.</td>
</tr>
<tr>
<td>Allow Unsigned Executable Memory<a href="#fn2" class="footnote-ref"
id="fnref2" role="doc-noteref"><sup>2</sup></a></td>
<td>Allows creating writable and executable memory without JIT
restrictions. If you are using add-ons with dynamic or self-modifying
native code, enable them according to the add-on documentation.</td>
</tr>
<tr>
<td>Allow DYLD Environment Variables<a href="#fn3" class="footnote-ref"
id="fnref3" role="doc-noteref"><sup>3</sup></a></td>
<td>Allows app to uss dynamic linker environment variables to inject
code. If you are using add-ons with dynamic or self-modifying native
code, enable them according to the add-on documentation.</td>
</tr>
<tr>
<td>Disable Library Validation</td>
<td>Allows app to load arbitrary libraries and frameworks. Enable it if
you are using GDExtension add-ons or ad-hoc signing, or want to support
user-provided external add-ons.</td>
</tr>
<tr>
<td>Audio Input</td>
<td>Enable if you need to use the microphone or other audio input
sources, if it's enabled you should also provide usage message in the
<span class="title-ref">privacy/microphone_usage_description</span>
option.</td>
</tr>
<tr>
<td>Camera</td>
<td>Enable if you need to use the camera, if it's enabled you should
also provide usage message in the <span
class="title-ref">privacy/camera_usage_description</span> option.</td>
</tr>
<tr>
<td>Location</td>
<td>Enable if you need to use location information from Location
Services, if it's enabled you should also provide usage message in the
<span class="title-ref">privacy/location_usage_description</span>
option.</td>
</tr>
<tr>
<td>Address Book</td>
<td><a href="#fn4" class="footnote-ref" id="fnref4"
role="doc-noteref"><sup>4</sup></a> Enable to allow access contacts in
the user's address book, if it's enabled you should also provide usage
message in the <span
class="title-ref">privacy/address_book_usage_description</span>
option.</td>
</tr>
<tr>
<td>Calendars</td>
<td><a href="#fn5" class="footnote-ref" id="fnref5"
role="doc-noteref"><sup>5</sup></a> Enable to allow access to the user's
calendar, if it's enabled you should also provide usage message in the
<span class="title-ref">privacy/calendar_usage_description</span>
option.</td>
</tr>
<tr>
<td>Photo Library</td>
<td><a href="#fn6" class="footnote-ref" id="fnref6"
role="doc-noteref"><sup>6</sup></a> Enable to allow access to the user's
Photos library, if it's enabled you should also provide usage message in
the <span
class="title-ref">privacy/photos_library_usage_description</span>
option.</td>
</tr>
<tr>
<td>Apple Events</td>
<td><a href="#fn7" class="footnote-ref" id="fnref7"
role="doc-noteref"><sup>7</sup></a> Enable to allow app to send Apple
events to other apps.</td>
</tr>
<tr>
<td>Debugging</td>
<td><a href="#fn8" class="footnote-ref" id="fnref8"
role="doc-noteref"><sup>8</sup></a> You can temporarily enable this
entitlement to use native debugger (GDB, LLDB) with the exported app.
This entitlement should be disabled for production export.</td>
</tr>
</tbody>
</table>
<section id="footnotes" class="footnotes footnotes-end-of-document"
role="doc-endnotes">
<hr />
<ol>
<li id="fn1"><p>The <code>Allow JIT Code Execution</code>,
<code>Allow Unsigned Executable Memory</code> and
<code>Allow DYLD Environment Variables</code> entitlements are always
enabled for the Godot Mono exports, and are not visible in the export
options.<a href="#fnref1" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
<li id="fn2"><p>The <code>Allow JIT Code Execution</code>,
<code>Allow Unsigned Executable Memory</code> and
<code>Allow DYLD Environment Variables</code> entitlements are always
enabled for the Godot Mono exports, and are not visible in the export
options.<a href="#fnref2" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
<li id="fn3"><p>The <code>Allow JIT Code Execution</code>,
<code>Allow Unsigned Executable Memory</code> and
<code>Allow DYLD Environment Variables</code> entitlements are always
enabled for the Godot Mono exports, and are not visible in the export
options.<a href="#fnref3" class="footnote-back"
role="doc-backlink">↩︎</a></p></li>
<li id="fn4"><p>These features aren't supported by Godot out of the box,
enable them only if you are using add-ons which require them.<a
href="#fnref4" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn5"><p>These features aren't supported by Godot out of the box,
enable them only if you are using add-ons which require them.<a
href="#fnref5" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn6"><p>These features aren't supported by Godot out of the box,
enable them only if you are using add-ons which require them.<a
href="#fnref6" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn7"><p>These features aren't supported by Godot out of the box,
enable them only if you are using add-ons which require them.<a
href="#fnref7" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn8"><p>To notarize an app, you must disable the
<code>Debugging</code> entitlement.<a href="#fnref8"
class="footnote-back" role="doc-backlink">↩︎</a></p></li>
</ol>
</section>

### App Sandbox Entitlement

The App Sandbox restricts access to user data, networking and devices.
Sandboxed apps can't access most of the file system, can't use custom
file dialogs and execute binaries (using `OS.execute` and
`OS.create_process`) outside the `.app` bundle. See [App
Sandbox](https://developer.apple.com/documentation/security/app_sandbox?language=objc)
for more info.

Note

To distribute an app through the App Store, you must enable the App
Sandbox.

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<thead>
<tr>
<th>Entitlement</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Enabled</td>
<td>Enables App Sandbox.</td>
</tr>
<tr>
<td>Network Server</td>
<td>Enable to allow app to listen for incoming network connections.</td>
</tr>
<tr>
<td>Network Client</td>
<td>Enable to allow app to establish outgoing network connections.</td>
</tr>
<tr>
<td>Device USB</td>
<td>Enable to allow app to interact with USB devices. This entitlement
is required to use wired controllers.</td>
</tr>
<tr>
<td>Device Bluetooth</td>
<td>Enable to allow app to interact with Bluetooth devices. This
entitlement is required to use wireless controllers.</td>
</tr>
<tr>
<td>Files Downloads<a href="#fn1" class="footnote-ref" id="fnref1"
role="doc-noteref"><sup>1</sup></a></td>
<td>Allows read or write access to the user's "Downloads" folder.</td>
</tr>
<tr>
<td>Files Pictures<a href="#fn2" class="footnote-ref" id="fnref2"
role="doc-noteref"><sup>2</sup></a></td>
<td>Allows read or write access to the user's "Pictures" folder.</td>
</tr>
<tr>
<td>Files Music<a href="#fn3" class="footnote-ref" id="fnref3"
role="doc-noteref"><sup>3</sup></a></td>
<td>Allows read or write access to the user's "Music" folder.</td>
</tr>
<tr>
<td>Files Movies<a href="#fn4" class="footnote-ref" id="fnref4"
role="doc-noteref"><sup>4</sup></a></td>
<td>Allows read or write access to the user's "Movies" folder.</td>
</tr>
<tr>
<td>Files User Selected<a href="#fn5" class="footnote-ref" id="fnref5"
role="doc-noteref"><sup>5</sup></a></td>
<td>Allows read or write access to arbitrary folder. To gain access, a
folder must be selected from the native file dialog by the user.</td>
</tr>
<tr>
<td>Helper Executable</td>
<td>List of helper executables to embedded to the app bundle. Sandboxed
app are limited to execute only these executable.</td>
</tr>
</tbody>
</table>
<section id="footnotes" class="footnotes footnotes-end-of-document"
role="doc-endnotes">
<hr />
<ol>
<li id="fn1"><p>You can optionally provide usage messages for various
folders in the <span
class="title-ref">privacy/*_folder_usage_description</span> options.<a
href="#fnref1" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn2"><p>You can optionally provide usage messages for various
folders in the <span
class="title-ref">privacy/*_folder_usage_description</span> options.<a
href="#fnref2" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn3"><p>You can optionally provide usage messages for various
folders in the <span
class="title-ref">privacy/*_folder_usage_description</span> options.<a
href="#fnref3" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn4"><p>You can optionally provide usage messages for various
folders in the <span
class="title-ref">privacy/*_folder_usage_description</span> options.<a
href="#fnref4" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
<li id="fn5"><p>You can optionally provide usage messages for various
folders in the <span
class="title-ref">privacy/*_folder_usage_description</span> options.<a
href="#fnref5" class="footnote-back" role="doc-backlink">↩︎</a></p></li>
</ol>
</section>

Note

You can override default entitlements by selecting custom entitlements
file, in this case all other entitlement are ignored.

## Environment variables

You can use the following environment variables to set export options
outside of the editor. During the export process, these override the
values that you set in the export menu.

<table>
<caption>macOS export environment variables</caption>
<thead>
<tr>
<th>Export option</th>
<th>Environment variable</th>
</tr>
</thead>
<tbody>
<tr>
<td>Encryption / Encryption Key</td>
<td><code>GODOT_SCRIPT_ENCRYPTION_KEY</code></td>
</tr>
<tr>
<td>Options / Codesign / Certificate File</td>
<td><code>GODOT_MACOS_CODESIGN_CERTIFICATE_FILE</code></td>
</tr>
<tr>
<td>Options / Codesign / Certificate Password</td>
<td><code>GODOT_MACOS_CODESIGN_CERTIFICATE_PASSWORD</code></td>
</tr>
<tr>
<td>Options / Codesign / Provisioning Profile</td>
<td><code>GODOT_MACOS_CODESIGN_PROVISIONING_PROFILE</code></td>
</tr>
<tr>
<td>Options / Notarization / API UUID</td>
<td><code>GODOT_MACOS_NOTARIZATION_API_UUID</code></td>
</tr>
<tr>
<td>Options / Notarization / API Key</td>
<td><code>GODOT_MACOS_NOTARIZATION_API_KEY</code></td>
</tr>
<tr>
<td>Options / Notarization / API Key ID</td>
<td><code>GODOT_MACOS_NOTARIZATION_API_KEY_ID</code></td>
</tr>
<tr>
<td>Options / Notarization / Apple ID Name</td>
<td><code>GODOT_MACOS_NOTARIZATION_APPLE_ID_NAME</code></td>
</tr>
<tr>
<td>Options / Notarization / Apple ID Password</td>
<td><code>GODOT_MACOS_NOTARIZATION_APPLE_ID_PASSWORD</code></td>
</tr>
</tbody>
</table>
