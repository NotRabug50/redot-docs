# Exporting for Android

This page describes how to export a Godot project to Android. If you're
looking to compile export template binaries from source instead, read
`doc_compiling_for_android`.

Exporting for Android has fewer requirements than compiling Godot for
Android. The following steps detail what is needed to set up the Android
SDK and the engine.

Attention

Projects written in C# can be exported to Android as of Godot 4.2, but
support is experimental and
`some limitations apply <doc_c_sharp_platforms>`.

## Install OpenJDK 17

Download and install [OpenJDK
17](https://adoptium.net/temurin/releases/?variant=openjdk17).

## Download the Android SDK

Download and install the Android SDK.

-   You can install the Android SDK using [Android Studio Iguana
    (version 2023.2.1) or later](https://developer.android.com/studio/).
    -   Run it once to complete the SDK setup using these
        [instructions](https://developer.android.com/studio/intro/update#sdk-manager).
    -   Ensure that the [required
        packages](https://developer.android.com/studio/intro/update#required)
        are installed as well.
        -   Android SDK Platform-Tools version 34.0.0 or later
        -   Android SDK Build-Tools version 34.0.0
        -   Android SDK Platform 34
        -   Android SDK Command-line Tools (latest)
    -   Ensure that the [NDK and CMake are installed and
        configured](https://developer.android.com/studio/projects/install-ndk).
        -   CMake version 3.10.2.4988404
        -   NDK version r23c (23.2.8568313)
-   Alternatively, you can install the Android SDK with the
    <span class="title-ref">sdkmanager</span> command line tool.
    -   Install the command line tools package using these
        [instructions](https://developer.android.com/tools/sdkmanager).
    -   Once the command line tools are installed, run the following
        <span class="title-ref">sdkmanager</span> command to complete
        the setup process:

<!-- -->

    sdkmanager --sdk_root=<android_sdk_path> "platform-tools" "build-tools;34.0.0" "platforms;android-34" "cmdline-tools;latest" "cmake;3.10.2.4988404" "ndk;23.2.8568313"

Note

If you are using Linux, **do not use an Android SDK provided by your
distribution's repositories as it will often be outdated**.

## Setting it up in Godot

Enter the Editor Settings screen. This screen contains the editor
settings for the user account in the computer (it's independent of the
project).

![image](img/editorsettings.png)

Scroll down to the section where the Android settings are located:

![image](img/android_editor_settings.webp)

In that screen, 2 paths need to be set:

-   `Java SDK Path` should be the location where OpenJDK 17 was
    installed.
-   `Android Sdk Path` should be the location where the Android SDK was
    installed.
    -   For example `%LOCALAPPDATA%\Android\Sdk\` on Windows or
        `/Users/$USER/Library/Android/sdk/` on macOS.

Once that is configured, everything is ready to export to Android!

Note

If you get an error saying *"Could not install to device."*, make sure
you do not have an application with the same Android package name
already installed on the device (but signed with a different key).

If you have an application with the same Android package name but a
different signing key already installed on the device, you **must**
remove the application in question from the Android device before
exporting to Android again.

## Providing launcher icons

Launcher icons are used by Android launcher apps to represent your
application to users. Godot only requires high-resolution icons (for
`xxxhdpi` density screens) and will automatically generate
lower-resolution variants.

There are two types of icons required by Godot:

-   **Main Icon:** The "classic" icon. This will be used on all Android
    versions up to Android 8 (Oreo), exclusive. Must be at least 192×192
    px.
-   **Adaptive Icons:** Starting from Android 8 (inclusive), [Adaptive
    Icons](https://developer.android.com/guide/practices/ui_guidelines/icon_design_adaptive)
    were introduced. Applications will need to include separate
    background and foreground icons to have a native look. The user's
    launcher application will control the icon's animation and masking.
    Must be at least 432×432 px.
-   **Themed Icons:** Starting from Android 13 (inclusive), Themed Icons
    were introduced. Applications will need to include a monochrome icon
    to enable this feature. The user's launcher application will control
    the icon's theme. Must be at least 432×432 px.

Caution

It is mandatory to provide a monochrome icon. Failure to do so will
result in the default Godot monochrome icon being used.

It's important to adhere to some rules when designing adaptive icons.
[Google Design has provided a nice
article](https://medium.com/google-design/designing-adaptive-icons-515af294c783)
that helps to understand those rules and some of the capabilities of
adaptive icons.

Caution

The most important adaptive icon design rule is to have your icon
critical elements inside the safe zone: a centered circle with a
diameter of 66dp (264 pixels on `xxxhdpi`) to avoid being clipped by the
launcher.

If you don't provide some of the requested icons, Godot will replace
them using a fallback chain, trying the next in line when the current
one fails:

-   **Main Icon:** Provided main icon -&gt; Project icon -&gt; Default
    Godot main icon.
-   **Adaptive Icon Foreground:** Provided foreground icon -&gt;
    Provided main icon -&gt; Project icon -&gt; Default Godot foreground
    icon.
-   **Adaptive Icon Background:** Provided background icon -&gt; Default
    Godot background icon.
-   **Adaptive Icon Monochrome:** Provided monochrome icon -&gt; Default
    Godot monochrome icon.

It's highly recommended to provide all the requested icons with their
specified resolutions. This way, your application will look great on all
Android devices and versions.

## Exporting for Google Play Store

Uploading an APK to Google's Play Store requires you to sign using a
non-debug keystore file; such file can be generated like this:

    keytool -v -genkey -keystore mygame.keystore -alias mygame -keyalg RSA -validity 10000

This keystore and key are used to verify your developer identity,
remember the password and keep it in a safe place! It is suggested to
use only upper and lowercase letters and numbers. Special characters may
cause errors. Use Google's Android Developer guides to learn more about
[APK signing](https://developer.android.com/studio/publish/app-signing).

Now fill in the following forms in your Android Export Presets:

![image](img/editor-export-presets-android.png)

-   **Release:** Enter the path to the keystore file you just generated.
-   **Release User:** Replace with the key alias.
-   **Release Password:** Key password. Note that the keystore password
    and the key password currently have to be the same.

Don't forget to uncheck the **Export With Debug** checkbox while
exporting.

![image](img/export-with-debug-button.png)

## Optimizing the APK size

By default, the APK will contain native libraries for both ARMv7 and
ARMv8 architectures. This increases its size significantly. To create a
smaller APK, uncheck either **Armeabi-v 7a** or **Arm 64 -v 8a** in your
project's Android export preset. This will create an APK that only
contains a library for a single architecture. Note that applications
targeting ARMv7 can also run on ARMv8 devices, but the opposite is not
true.

Since August 2019, Google Play requires all applications to be available
in 64-bit form. This means you cannot upload an APK that contains *just*
an ARMv7 library. To solve this, you can upload several APKs to Google
Play using its [Multiple APK
support](https://developer.android.com/google/play/publishing/multiple-apks).
Each APK should target a single architecture; creating an APK for ARMv7
and ARMv8 is usually sufficient to cover most devices in use today.

You can optimize the size further by compiling an Android export
template with only the features you need. See `doc_optimizing_for_size`
for more information.

## Environment variables

You can use the following environment variables to set export options
outside of the editor. During the export process, these override the
values that you set in the export menu.

<table>
<caption>Android export environment variables</caption>
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
<td>Options / Keystore / Debug</td>
<td><code>GODOT_ANDROID_KEYSTORE_DEBUG_PATH</code></td>
</tr>
<tr>
<td>Options / Keystore / Debug User</td>
<td><code>GODOT_ANDROID_KEYSTORE_DEBUG_USER</code></td>
</tr>
<tr>
<td>Options / Keystore / Debug Password</td>
<td><code>GODOT_ANDROID_KEYSTORE_DEBUG_PASSWORD</code></td>
</tr>
<tr>
<td>Options / Keystore / Release</td>
<td><code>GODOT_ANDROID_KEYSTORE_RELEASE_PATH</code></td>
</tr>
<tr>
<td>Options / Keystore / Release User</td>
<td><code>GODOT_ANDROID_KEYSTORE_RELEASE_USER</code></td>
</tr>
<tr>
<td>Options / Keystore / Release Password</td>
<td><code>GODOT_ANDROID_KEYSTORE_RELEASE_PASSWORD</code></td>
</tr>
</tbody>
</table>
