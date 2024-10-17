github\_url  
hide

# EditorExportPlatformAndroid

**Inherits:** `EditorExportPlatform<class_EditorExportPlatform>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Exporter for Android.

classref-introduction-group

## Tutorials

-   `Exporting for Android <../tutorials/export/exporting_for_android>`
-   `Gradle builds for Android <../tutorials/export/android_gradle_build>`
-   `Android plugins documentation index <../tutorials/platform/index>`

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

`String<class_String>` **apk\_expansion/SALT**
`🔗<class_EditorExportPlatformAndroid_property_apk_expansion/SALT>`

Array of random bytes that the licensing Policy uses to create an
[Obfuscator](https://developer.android.com/google/play/licensing/adding-licensing#impl-Obfuscator).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **apk\_expansion/enable**
`🔗<class_EditorExportPlatformAndroid_property_apk_expansion/enable>`

If `true`, project resources are stored in the separate APK expansion
file, instead of the APK.

\*\*Note:\*\* APK expansion should be enabled to use PCK encryption. See
[APK Expansion
Files](https://developer.android.com/google/play/expansion-files)

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **apk\_expansion/public\_key**
`🔗<class_EditorExportPlatformAndroid_property_apk_expansion/public_key>`

Base64 encoded RSA public key for your publisher account, available from
the profile page on the "Google Play Console".

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **architectures/arm64-v8a**
`🔗<class_EditorExportPlatformAndroid_property_architectures/arm64-v8a>`

If `true`, `arm64` binaries are included into exported project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **architectures/armeabi-v7a**
`🔗<class_EditorExportPlatformAndroid_property_architectures/armeabi-v7a>`

If `true`, `arm32` binaries are included into exported project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **architectures/x86**
`🔗<class_EditorExportPlatformAndroid_property_architectures/x86>`

If `true`, `x86_32` binaries are included into exported project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **architectures/x86\_64**
`🔗<class_EditorExportPlatformAndroid_property_architectures/x86_64>`

If `true`, `x86_64` binaries are included into exported project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **command\_line/extra\_args**
`🔗<class_EditorExportPlatformAndroid_property_command_line/extra_args>`

A list of additional command line arguments, separated by space, which
the exported project will receive when started.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_template/debug**
`🔗<class_EditorExportPlatformAndroid_property_custom_template/debug>`

Path to an APK file to use as a custom export template for debug
exports. If left empty, default template is used.

\*\*Note:\*\* This is only used if
`gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_template/release**
`🔗<class_EditorExportPlatformAndroid_property_custom_template/release>`

Path to an APK file to use as a custom export template for release
exports. If left empty, default template is used.

\*\*Note:\*\* This is only used if
`gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **gradle\_build/android\_source\_template**
`🔗<class_EditorExportPlatformAndroid_property_gradle_build/android_source_template>`

Path to a ZIP file holding the source for the export template used in a
Gradle build. If left empty, the default template is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gradle\_build/compress\_native\_libraries**
`🔗<class_EditorExportPlatformAndroid_property_gradle_build/compress_native_libraries>`

If `true`, native libraries are compressed when performing a Gradle
build.

\*\*Note:\*\* Although your binary may be smaller, your application may
load slower because the native libraries are not loaded directly from
the binary at runtime.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **gradle\_build/export\_format**
`🔗<class_EditorExportPlatformAndroid_property_gradle_build/export_format>`

Application export format (\*.apk or \*.aab).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **gradle\_build/gradle\_build\_directory**
`🔗<class_EditorExportPlatformAndroid_property_gradle_build/gradle_build_directory>`

Path to the Gradle build directory. If left empty, then `res://android`
will be used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **gradle\_build/min\_sdk**
`🔗<class_EditorExportPlatformAndroid_property_gradle_build/min_sdk>`

Minimum Android API level required for the application to run (used
during Gradle build). See
[android:minSdkVersion](https://developer.android.com/guide/topics/manifest/uses-sdk-element#uses).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **gradle\_build/target\_sdk**
`🔗<class_EditorExportPlatformAndroid_property_gradle_build/target_sdk>`

The Android API level on which the application is designed to run (used
during Gradle build). See
[android:targetSdkVersion](https://developer.android.com/guide/topics/manifest/uses-sdk-element#uses).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gradle\_build/use\_gradle\_build**
`🔗<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`

If `true`, Gradle build is used instead of pre-built APK.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **graphics/opengl\_debug**
`🔗<class_EditorExportPlatformAndroid_property_graphics/opengl_debug>`

If `true`, OpenGL ES debug context will be created (additional runtime
checking, validation, and logging).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **keystore/debug**
`🔗<class_EditorExportPlatformAndroid_property_keystore/debug>`

Path of the debug keystore file.

Can be overridden with the environment variable
`GODOT_ANDROID_KEYSTORE_DEBUG_PATH`.

Fallbacks to `EditorSettings.export/android/debug_keystore` if empty.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **keystore/debug\_password**
`🔗<class_EditorExportPlatformAndroid_property_keystore/debug_password>`

Password for the debug keystore file.

Can be overridden with the environment variable
`GODOT_ANDROID_KEYSTORE_DEBUG_PASSWORD`.

Fallbacks to `EditorSettings.export/android/debug_keystore_pass` if both
it and
`keystore/debug<class_EditorExportPlatformAndroid_property_keystore/debug>`
are empty.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **keystore/debug\_user**
`🔗<class_EditorExportPlatformAndroid_property_keystore/debug_user>`

User name for the debug keystore file.

Can be overridden with the environment variable
`GODOT_ANDROID_KEYSTORE_DEBUG_USER`.

Fallbacks to `EditorSettings.export/android/debug_keystore_user` if both
it and
`keystore/debug<class_EditorExportPlatformAndroid_property_keystore/debug>`
are empty.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **keystore/release**
`🔗<class_EditorExportPlatformAndroid_property_keystore/release>`

Path of the release keystore file.

Can be overridden with the environment variable
`GODOT_ANDROID_KEYSTORE_RELEASE_PATH`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **keystore/release\_password**
`🔗<class_EditorExportPlatformAndroid_property_keystore/release_password>`

Password for the release keystore file.

Can be overridden with the environment variable
`GODOT_ANDROID_KEYSTORE_RELEASE_PASSWORD`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **keystore/release\_user**
`🔗<class_EditorExportPlatformAndroid_property_keystore/release_user>`

User name for the release keystore file.

Can be overridden with the environment variable
`GODOT_ANDROID_KEYSTORE_RELEASE_USER`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **launcher\_icons/adaptive\_background\_432x432**
`🔗<class_EditorExportPlatformAndroid_property_launcher_icons/adaptive_background_432x432>`

Background layer of the application adaptive icon file. See [Design
adaptive
icons](https://developer.android.com/develop/ui/views/launch/icon_design_adaptive#design-adaptive-icons).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **launcher\_icons/adaptive\_foreground\_432x432**
`🔗<class_EditorExportPlatformAndroid_property_launcher_icons/adaptive_foreground_432x432>`

Foreground layer of the application adaptive icon file. See [Design
adaptive
icons](https://developer.android.com/develop/ui/views/launch/icon_design_adaptive#design-adaptive-icons).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **launcher\_icons/adaptive\_monochrome\_432x432**
`🔗<class_EditorExportPlatformAndroid_property_launcher_icons/adaptive_monochrome_432x432>`

Monochrome layer of the application adaptive icon file. See [Design
adaptive
icons](https://developer.android.com/develop/ui/views/launch/icon_design_adaptive#design-adaptive-icons).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **launcher\_icons/main\_192x192**
`🔗<class_EditorExportPlatformAndroid_property_launcher_icons/main_192x192>`

Application icon file. If left empty, it will fallback to
`ProjectSettings.application/config/icon<class_ProjectSettings_property_application/config/icon>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **package/app\_category**
`🔗<class_EditorExportPlatformAndroid_property_package/app_category>`

Application category for the Google Play Store. Only define this if your
application fits one of the categories well. See
[android:appCategory](https://developer.android.com/guide/topics/manifest/application-element#appCategory).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **package/exclude\_from\_recents**
`🔗<class_EditorExportPlatformAndroid_property_package/exclude_from_recents>`

If `true`, task initiated by main activity will be excluded from the
list of recently used applications. See
[android:excludeFromRecents](https://developer.android.com/guide/topics/manifest/activity-element#exclude).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **package/name**
`🔗<class_EditorExportPlatformAndroid_property_package/name>`

Name of the application.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **package/retain\_data\_on\_uninstall**
`🔗<class_EditorExportPlatformAndroid_property_package/retain_data_on_uninstall>`

If `true`, when the user uninstalls an app, a prompt to keep the app's
data will be shown. See
[android:hasFragileUserData](https://developer.android.com/guide/topics/manifest/application-element#fragileuserdata).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **package/show\_as\_launcher\_app**
`🔗<class_EditorExportPlatformAndroid_property_package/show_as_launcher_app>`

If `true`, the user will be able to set this app as the system launcher
in Android preferences.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **package/show\_in\_android\_tv**
`🔗<class_EditorExportPlatformAndroid_property_package/show_in_android_tv>`

If `true`, this app will show in Android TV launcher UI.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **package/show\_in\_app\_library**
`🔗<class_EditorExportPlatformAndroid_property_package/show_in_app_library>`

If `true`, this app will show in the device's app library.

\*\*Note:\*\* This is `true` by default.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **package/signed**
`🔗<class_EditorExportPlatformAndroid_property_package/signed>`

If `true`, package signing is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **package/unique\_name**
`🔗<class_EditorExportPlatformAndroid_property_package/unique_name>`

Unique application identifier in a reverse-DNS format. The reverse DNS
format should preferably match a domain name you control, but this is
not strictly required. For instance, if you own `example.com`, your
package unique name should preferably be of the form
`com.example.mygame`. This identifier can only contain lowercase
alphanumeric characters (`a-z`, and `0-9`), underscores (`_`), and
periods (`.`). Each component of the reverse DNS format must start with
a letter: for instance, `com.example.8game` is not valid.

If `$genname` is present in the value, it will be replaced by the
project name converted to lowercase. If there are invalid characters in
the project name, they will be stripped. If all characters in the
project name are stripped, `$genname` is replaced by `noname`.

\*\*Note:\*\* Changing the package name will cause the package to be
considered as a new package, with its own installation and data paths.
The new package won't be usable to update existing installations.

\*\*Note:\*\* When publishing to Google Play, the package name must be
*globally* unique. This means no other apps published on Google Play
must be using the same package name as yours. Otherwise, you'll be
prevented from publishing your app on Google Play.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_checkin\_properties**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_checkin_properties>`

Allows read/write access to the "properties" table in the checkin
database. See
[ACCESS\_CHECKIN\_PROPERTIES](https://developer.android.com/reference/android/Manifest.permission#ACCESS_CHECKIN_PROPERTIES).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_coarse\_location**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_coarse_location>`

Allows access to the approximate location information. See
[ACCESS\_COARSE\_LOCATION](https://developer.android.com/reference/android/Manifest.permission#ACCESS_COARSE_LOCATION).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_fine\_location**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_fine_location>`

Allows access to the precise location information. See
[ACCESS\_FINE\_LOCATION](https://developer.android.com/reference/android/Manifest.permission#ACCESS_FINE_LOCATION).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_location\_extra\_commands**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_location_extra_commands>`

Allows access to the extra location provider commands. See
[ACCESS\_LOCATION\_EXTRA\_COMMANDS](https://developer.android.com/reference/android/Manifest.permission#ACCESS_LOCATION_EXTRA_COMMANDS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_mock\_location**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_mock_location>`

Allows an application to create mock location providers for testing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_network\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_network_state>`

Allows access to the information about networks. See
[ACCESS\_NETWORK\_STATE](https://developer.android.com/reference/android/Manifest.permission#ACCESS_NETWORK_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_surface\_flinger**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_surface_flinger>`

Allows an application to use SurfaceFlinger's low level features.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/access\_wifi\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/access_wifi_state>`

Allows access to the information about Wi-Fi networks. See
[ACCESS\_WIFI\_STATE](https://developer.android.com/reference/android/Manifest.permission#ACCESS_WIFI_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/account\_manager**
`🔗<class_EditorExportPlatformAndroid_property_permissions/account_manager>`

Allows applications to call into AccountAuthenticators. See
[ACCOUNT\_MANAGER](https://developer.android.com/reference/android/Manifest.permission#ACCOUNT_MANAGER).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/add\_voicemail**
`🔗<class_EditorExportPlatformAndroid_property_permissions/add_voicemail>`

Allows an application to add voicemails into the system. See
[ADD\_VOICEMAIL](https://developer.android.com/reference/android/Manifest.permission#ADD_VOICEMAIL).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/authenticate\_accounts**
`🔗<class_EditorExportPlatformAndroid_property_permissions/authenticate_accounts>`

Allows an application to act as an AccountAuthenticator for the
AccountManager.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/battery\_stats**
`🔗<class_EditorExportPlatformAndroid_property_permissions/battery_stats>`

Allows an application to collect battery statistics. See
[BATTERY\_STATS](https://developer.android.com/reference/android/Manifest.permission#BATTERY_STATS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_accessibility\_service**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_accessibility_service>`

Must be required by an AccessibilityService, to ensure that only the
system can bind to it. See
[BIND\_ACCESSIBILITY\_SERVICE](https://developer.android.com/reference/android/Manifest.permission#BIND_ACCESSIBILITY_SERVICE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_appwidget**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_appwidget>`

Allows an application to tell the AppWidget service which application
can access AppWidget's data. See
[BIND\_APPWIDGET](https://developer.android.com/reference/android/Manifest.permission#BIND_APPWIDGET).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_device\_admin**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_device_admin>`

Must be required by device administration receiver, to ensure that only
the system can interact with it. See
[BIND\_DEVICE\_ADMIN](https://developer.android.com/reference/android/Manifest.permission#BIND_DEVICE_ADMIN).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_input\_method**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_input_method>`

Must be required by an InputMethodService, to ensure that only the
system can bind to it. See
[BIND\_INPUT\_METHOD](https://developer.android.com/reference/android/Manifest.permission#BIND_INPUT_METHOD).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_nfc\_service**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_nfc_service>`

Must be required by a HostApduService or OffHostApduService to ensure
that only the system can bind to it. See
[BIND\_NFC\_SERVICE](https://developer.android.com/reference/android/Manifest.permission#BIND_NFC_SERVICE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_notification\_listener\_service**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_notification_listener_service>`

Must be required by a NotificationListenerService, to ensure that only
the system can bind to it. See
[BIND\_NOTIFICATION\_LISTENER\_SERVICE](https://developer.android.com/reference/android/Manifest.permission#BIND_NOTIFICATION_LISTENER_SERVICE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_print\_service**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_print_service>`

Must be required by a PrintService, to ensure that only the system can
bind to it. See
[BIND\_PRINT\_SERVICE](https://developer.android.com/reference/android/Manifest.permission#BIND_PRINT_SERVICE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_remoteviews**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_remoteviews>`

Must be required by a RemoteViewsService, to ensure that only the system
can bind to it. See
[BIND\_REMOTEVIEWS](https://developer.android.com/reference/android/Manifest.permission#BIND_REMOTEVIEWS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_text\_service**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_text_service>`

Must be required by a TextService (e.g. SpellCheckerService) to ensure
that only the system can bind to it. See
[BIND\_TEXT\_SERVICE](https://developer.android.com/reference/android/Manifest.permission#BIND_TEXT_SERVICE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_vpn\_service**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_vpn_service>`

Must be required by a VpnService, to ensure that only the system can
bind to it. See
[BIND\_VPN\_SERVICE](https://developer.android.com/reference/android/Manifest.permission#BIND_VPN_SERVICE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bind\_wallpaper**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bind_wallpaper>`

Must be required by a WallpaperService, to ensure that only the system
can bind to it. See
[BIND\_WALLPAPER](https://developer.android.com/reference/android/Manifest.permission#BIND_WALLPAPER).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bluetooth**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bluetooth>`

Allows applications to connect to paired bluetooth devices. See
[BLUETOOTH](https://developer.android.com/reference/android/Manifest.permission#BLUETOOTH).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bluetooth\_admin**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bluetooth_admin>`

Allows applications to discover and pair bluetooth devices. See
[BLUETOOTH\_ADMIN](https://developer.android.com/reference/android/Manifest.permission#BLUETOOTH_ADMIN).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/bluetooth\_privileged**
`🔗<class_EditorExportPlatformAndroid_property_permissions/bluetooth_privileged>`

Allows applications to pair bluetooth devices without user interaction,
and to allow or disallow phonebook access or message access. See
[BLUETOOTH\_PRIVILEGED](https://developer.android.com/reference/android/Manifest.permission#BLUETOOTH_PRIVILEGED).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/brick**
`🔗<class_EditorExportPlatformAndroid_property_permissions/brick>`

Required to be able to disable the device (very dangerous!).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/broadcast\_package\_removed**
`🔗<class_EditorExportPlatformAndroid_property_permissions/broadcast_package_removed>`

Allows an application to broadcast a notification that an application
package has been removed. See
[BROADCAST\_PACKAGE\_REMOVED](https://developer.android.com/reference/android/Manifest.permission#BROADCAST_PACKAGE_REMOVED).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/broadcast\_sms**
`🔗<class_EditorExportPlatformAndroid_property_permissions/broadcast_sms>`

Allows an application to broadcast an SMS receipt notification. See
[BROADCAST\_SMS](https://developer.android.com/reference/android/Manifest.permission#BROADCAST_SMS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/broadcast\_sticky**
`🔗<class_EditorExportPlatformAndroid_property_permissions/broadcast_sticky>`

Allows an application to broadcast sticky intents. See
[BROADCAST\_STICKY](https://developer.android.com/reference/android/Manifest.permission#BROADCAST_STICKY).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/broadcast\_wap\_push**
`🔗<class_EditorExportPlatformAndroid_property_permissions/broadcast_wap_push>`

Allows an application to broadcast a WAP PUSH receipt notification. See
[BROADCAST\_WAP\_PUSH](https://developer.android.com/reference/android/Manifest.permission#BROADCAST_WAP_PUSH).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/call\_phone**
`🔗<class_EditorExportPlatformAndroid_property_permissions/call_phone>`

Allows an application to initiate a phone call without going through the
Dialer user interface. See
[CALL\_PHONE](https://developer.android.com/reference/android/Manifest.permission#CALL_PHONE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/call\_privileged**
`🔗<class_EditorExportPlatformAndroid_property_permissions/call_privileged>`

Allows an application to call any phone number, including emergency
numbers, without going through the Dialer user interface. See
[CALL\_PRIVILEGED](https://developer.android.com/reference/android/Manifest.permission#CALL_PRIVILEGED).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/camera**
`🔗<class_EditorExportPlatformAndroid_property_permissions/camera>`

Required to be able to access the camera device. See
[CAMERA](https://developer.android.com/reference/android/Manifest.permission#CAMERA).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/capture\_audio\_output**
`🔗<class_EditorExportPlatformAndroid_property_permissions/capture_audio_output>`

Allows an application to capture audio output. See
[CAPTURE\_AUDIO\_OUTPUT](https://developer.android.com/reference/android/Manifest.permission#CAPTURE_AUDIO_OUTPUT).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/capture\_secure\_video\_output**
`🔗<class_EditorExportPlatformAndroid_property_permissions/capture_secure_video_output>`

Allows an application to capture secure video output.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/capture\_video\_output**
`🔗<class_EditorExportPlatformAndroid_property_permissions/capture_video_output>`

Allows an application to capture video output.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/change\_component\_enabled\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/change_component_enabled_state>`

Allows an application to change whether an application component (other
than its own) is enabled or not. See
[CHANGE\_COMPONENT\_ENABLED\_STATE](https://developer.android.com/reference/android/Manifest.permission#CHANGE_COMPONENT_ENABLED_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/change\_configuration**
`🔗<class_EditorExportPlatformAndroid_property_permissions/change_configuration>`

Allows an application to modify the current configuration, such as
locale. See
[CHANGE\_CONFIGURATION](https://developer.android.com/reference/android/Manifest.permission#CHANGE_CONFIGURATION).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/change\_network\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/change_network_state>`

Allows applications to change network connectivity state. See
[CHANGE\_NETWORK\_STATE](https://developer.android.com/reference/android/Manifest.permission#CHANGE_NETWORK_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/change\_wifi\_multicast\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/change_wifi_multicast_state>`

Allows applications to enter Wi-Fi Multicast mode. See
[CHANGE\_WIFI\_MULTICAST\_STATE](https://developer.android.com/reference/android/Manifest.permission#CHANGE_WIFI_MULTICAST_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/change\_wifi\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/change_wifi_state>`

Allows applications to change Wi-Fi connectivity state. See
[CHANGE\_WIFI\_STATE](https://developer.android.com/reference/android/Manifest.permission#CHANGE_WIFI_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/clear\_app\_cache**
`🔗<class_EditorExportPlatformAndroid_property_permissions/clear_app_cache>`

Allows an application to clear the caches of all installed applications
on the device. See
[CLEAR\_APP\_CACHE](https://developer.android.com/reference/android/Manifest.permission#CLEAR_APP_CACHE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/clear\_app\_user\_data**
`🔗<class_EditorExportPlatformAndroid_property_permissions/clear_app_user_data>`

Allows an application to clear user data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/control\_location\_updates**
`🔗<class_EditorExportPlatformAndroid_property_permissions/control_location_updates>`

Allows enabling/disabling location update notifications from the radio.
See
[CONTROL\_LOCATION\_UPDATES](https://developer.android.com/reference/android/Manifest.permission#CONTROL_LOCATION_UPDATES).

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>`
**permissions/custom\_permissions**
`🔗<class_EditorExportPlatformAndroid_property_permissions/custom_permissions>`

Array of custom permission strings.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/delete\_cache\_files**
`🔗<class_EditorExportPlatformAndroid_property_permissions/delete_cache_files>`

**Deprecated:** This property may be changed or removed in future
versions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/delete\_packages**
`🔗<class_EditorExportPlatformAndroid_property_permissions/delete_packages>`

Allows an application to delete packages. See
[DELETE\_PACKAGES](https://developer.android.com/reference/android/Manifest.permission#DELETE_PACKAGES).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/device\_power**
`🔗<class_EditorExportPlatformAndroid_property_permissions/device_power>`

Allows low-level access to power management.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/diagnostic**
`🔗<class_EditorExportPlatformAndroid_property_permissions/diagnostic>`

Allows applications to RW to diagnostic resources. See
[DIAGNOSTIC](https://developer.android.com/reference/android/Manifest.permission#DIAGNOSTIC).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/disable\_keyguard**
`🔗<class_EditorExportPlatformAndroid_property_permissions/disable_keyguard>`

Allows applications to disable the keyguard if it is not secure. See
[DISABLE\_KEYGUARD](https://developer.android.com/reference/android/Manifest.permission#DISABLE_KEYGUARD).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/dump**
`🔗<class_EditorExportPlatformAndroid_property_permissions/dump>`

Allows an application to retrieve state dump information from system
services. See
[DUMP](https://developer.android.com/reference/android/Manifest.permission#DUMP).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/expand\_status\_bar**
`🔗<class_EditorExportPlatformAndroid_property_permissions/expand_status_bar>`

Allows an application to expand or collapse the status bar. See
[EXPAND\_STATUS\_BAR](https://developer.android.com/reference/android/Manifest.permission#EXPAND_STATUS_BAR).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/factory\_test**
`🔗<class_EditorExportPlatformAndroid_property_permissions/factory_test>`

Run as a manufacturer test application, running as the root user. See
[FACTORY\_TEST](https://developer.android.com/reference/android/Manifest.permission#FACTORY_TEST).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/flashlight**
`🔗<class_EditorExportPlatformAndroid_property_permissions/flashlight>`

Allows access to the flashlight.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/force\_back**
`🔗<class_EditorExportPlatformAndroid_property_permissions/force_back>`

Allows an application to force a BACK operation on whatever is the top
activity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/get\_accounts**
`🔗<class_EditorExportPlatformAndroid_property_permissions/get_accounts>`

Allows access to the list of accounts in the Accounts Service. See
[GET\_ACCOUNTS](https://developer.android.com/reference/android/Manifest.permission#GET_ACCOUNTS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/get\_package\_size**
`🔗<class_EditorExportPlatformAndroid_property_permissions/get_package_size>`

Allows an application to find out the space used by any package. See
[GET\_PACKAGE\_SIZE](https://developer.android.com/reference/android/Manifest.permission#GET_PACKAGE_SIZE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/get\_tasks**
`🔗<class_EditorExportPlatformAndroid_property_permissions/get_tasks>`

**Deprecated:** Deprecated in API level 21.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/get\_top\_activity\_info**
`🔗<class_EditorExportPlatformAndroid_property_permissions/get_top_activity_info>`

Allows an application to retrieve private information about the current
top activity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/global\_search**
`🔗<class_EditorExportPlatformAndroid_property_permissions/global_search>`

Used on content providers to allow the global search system to access
their data. See
[GLOBAL\_SEARCH](https://developer.android.com/reference/android/Manifest.permission#GLOBAL_SEARCH).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/hardware\_test**
`🔗<class_EditorExportPlatformAndroid_property_permissions/hardware_test>`

Allows access to hardware peripherals.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/inject\_events**
`🔗<class_EditorExportPlatformAndroid_property_permissions/inject_events>`

Allows an application to inject user events (keys, touch, trackball)
into the event stream and deliver them to ANY window.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/install\_location\_provider**
`🔗<class_EditorExportPlatformAndroid_property_permissions/install_location_provider>`

Allows an application to install a location provider into the Location
Manager. See
[INSTALL\_LOCATION\_PROVIDER](https://developer.android.com/reference/android/Manifest.permission#INSTALL_LOCATION_PROVIDER).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/install\_packages**
`🔗<class_EditorExportPlatformAndroid_property_permissions/install_packages>`

Allows an application to install packages. See
[INSTALL\_PACKAGES](https://developer.android.com/reference/android/Manifest.permission#INSTALL_PACKAGES).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/install\_shortcut**
`🔗<class_EditorExportPlatformAndroid_property_permissions/install_shortcut>`

Allows an application to install a shortcut in Launcher. See
[INSTALL\_SHORTCUT](https://developer.android.com/reference/android/Manifest.permission#INSTALL_SHORTCUT).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/internal\_system\_window**
`🔗<class_EditorExportPlatformAndroid_property_permissions/internal_system_window>`

Allows an application to open windows that are for use by parts of the
system user interface.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/internet**
`🔗<class_EditorExportPlatformAndroid_property_permissions/internet>`

Allows applications to open network sockets. See
[INTERNET](https://developer.android.com/reference/android/Manifest.permission#INTERNET).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/kill\_background\_processes**
`🔗<class_EditorExportPlatformAndroid_property_permissions/kill_background_processes>`

Allows an application to call
ActivityManager.killBackgroundProcesses(String). See
[KILL\_BACKGROUND\_PROCESSES](https://developer.android.com/reference/android/Manifest.permission#KILL_BACKGROUND_PROCESSES).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/location\_hardware**
`🔗<class_EditorExportPlatformAndroid_property_permissions/location_hardware>`

Allows an application to use location features in hardware, such as the
geofencing api. See
[LOCATION\_HARDWARE](https://developer.android.com/reference/android/Manifest.permission#LOCATION_HARDWARE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/manage\_accounts**
`🔗<class_EditorExportPlatformAndroid_property_permissions/manage_accounts>`

Allows an application to manage the list of accounts in the
AccountManager.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/manage\_app\_tokens**
`🔗<class_EditorExportPlatformAndroid_property_permissions/manage_app_tokens>`

Allows an application to manage (create, destroy, Z-order) application
tokens in the window manager.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/manage\_documents**
`🔗<class_EditorExportPlatformAndroid_property_permissions/manage_documents>`

Allows an application to manage access to documents, usually as part of
a document picker. See
[MANAGE\_DOCUMENTS](https://developer.android.com/reference/android/Manifest.permission#MANAGE_DOCUMENTS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/manage\_external\_storage**
`🔗<class_EditorExportPlatformAndroid_property_permissions/manage_external_storage>`

Allows an application a broad access to external storage in scoped
storage. See
[MANAGE\_EXTERNAL\_STORAGE](https://developer.android.com/reference/android/Manifest.permission#MANAGE_EXTERNAL_STORAGE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/master\_clear**
`🔗<class_EditorExportPlatformAndroid_property_permissions/master_clear>`

See
[MASTER\_CLEAR](https://developer.android.com/reference/android/Manifest.permission#MASTER_CLEAR).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/media\_content\_control**
`🔗<class_EditorExportPlatformAndroid_property_permissions/media_content_control>`

Allows an application to know what content is playing and control its
playback. See
[MEDIA\_CONTENT\_CONTROL](https://developer.android.com/reference/android/Manifest.permission#MEDIA_CONTENT_CONTROL).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/modify\_audio\_settings**
`🔗<class_EditorExportPlatformAndroid_property_permissions/modify_audio_settings>`

Allows an application to modify global audio settings. See
[MODIFY\_AUDIO\_SETTINGS](https://developer.android.com/reference/android/Manifest.permission#MODIFY_AUDIO_SETTINGS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/modify\_phone\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/modify_phone_state>`

Allows modification of the telephony state - power on, mmi, etc. Does
not include placing calls. See
[MODIFY\_PHONE\_STATE](https://developer.android.com/reference/android/Manifest.permission#MODIFY_PHONE_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/mount\_format\_filesystems**
`🔗<class_EditorExportPlatformAndroid_property_permissions/mount_format_filesystems>`

Allows formatting file systems for removable storage. See
[MOUNT\_FORMAT\_FILESYSTEMS](https://developer.android.com/reference/android/Manifest.permission#MOUNT_FORMAT_FILESYSTEMS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/mount\_unmount\_filesystems**
`🔗<class_EditorExportPlatformAndroid_property_permissions/mount_unmount_filesystems>`

Allows mounting and unmounting file systems for removable storage. See
[MOUNT\_UNMOUNT\_FILESYSTEMS](https://developer.android.com/reference/android/Manifest.permission#MOUNT_UNMOUNT_FILESYSTEMS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/nfc**
`🔗<class_EditorExportPlatformAndroid_property_permissions/nfc>`

Allows applications to perform I/O operations over NFC. See
[NFC](https://developer.android.com/reference/android/Manifest.permission#NFC).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/persistent\_activity**
`🔗<class_EditorExportPlatformAndroid_property_permissions/persistent_activity>`

**Deprecated:** Deprecated in API level 15.

Allows an application to make its activities persistent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/post\_notifications**
`🔗<class_EditorExportPlatformAndroid_property_permissions/post_notifications>`

Allows an application to post notifications. Added in API level 33. See
[Notification runtime
permission](https://developer.android.com/develop/ui/views/notifications/notification-permission).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/process\_outgoing\_calls**
`🔗<class_EditorExportPlatformAndroid_property_permissions/process_outgoing_calls>`

**Deprecated:** Deprecated in API level 29.

Allows an application to see the number being dialed during an outgoing
call with the option to redirect the call to a different number or abort
the call altogether. See
[PROCESS\_OUTGOING\_CALLS](https://developer.android.com/reference/android/Manifest.permission#PROCESS_OUTGOING_CALLS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_calendar**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_calendar>`

Allows an application to read the user's calendar data. See
[READ\_CALENDAR](https://developer.android.com/reference/android/Manifest.permission#READ_CALENDAR).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_call\_log**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_call_log>`

Allows an application to read the user's call log. See
[READ\_CALL\_LOG](https://developer.android.com/reference/android/Manifest.permission#READ_CALL_LOG).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_contacts**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_contacts>`

Allows an application to read the user's contacts data. See
[READ\_CONTACTS](https://developer.android.com/reference/android/Manifest.permission#READ_CONTACTS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_external\_storage**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_external_storage>`

**Deprecated:** Deprecated in API level 33.

Allows an application to read from external storage. See
[READ\_EXTERNAL\_STORAGE](https://developer.android.com/reference/android/Manifest.permission#READ_EXTERNAL_STORAGE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_frame\_buffer**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_frame_buffer>`

Allows an application to take screen shots and more generally get access
to the frame buffer data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_history\_bookmarks**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_history_bookmarks>`

Allows an application to read (but not write) the user's browsing
history and bookmarks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_input\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_input_state>`

**Deprecated:** Deprecated in API level 16.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_logs**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_logs>`

Allows an application to read the low-level system log files. See
[READ\_LOGS](https://developer.android.com/reference/android/Manifest.permission#READ_LOGS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_phone\_state**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_phone_state>`

Allows read only access to phone state. See
[READ\_PHONE\_STATE](https://developer.android.com/reference/android/Manifest.permission#READ_PHONE_STATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_profile**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_profile>`

Allows an application to read the user's personal profile data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_sms**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_sms>`

Allows an application to read SMS messages. See
[READ\_SMS](https://developer.android.com/reference/android/Manifest.permission#READ_SMS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_social\_stream**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_social_stream>`

Allows an application to read from the user's social stream.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_sync\_settings**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_sync_settings>`

Allows applications to read the sync settings. See
[READ\_SYNC\_SETTINGS](https://developer.android.com/reference/android/Manifest.permission#READ_SYNC_SETTINGS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_sync\_stats**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_sync_stats>`

Allows applications to read the sync stats. See
[READ\_SYNC\_STATS](https://developer.android.com/reference/android/Manifest.permission#READ_SYNC_STATS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/read\_user\_dictionary**
`🔗<class_EditorExportPlatformAndroid_property_permissions/read_user_dictionary>`

Allows an application to read the user dictionary.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/reboot**
`🔗<class_EditorExportPlatformAndroid_property_permissions/reboot>`

Required to be able to reboot the device. See
[REBOOT](https://developer.android.com/reference/android/Manifest.permission#REBOOT).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/receive\_boot\_completed**
`🔗<class_EditorExportPlatformAndroid_property_permissions/receive_boot_completed>`

Allows an application to receive the Intent.ACTION\_BOOT\_COMPLETED that
is broadcast after the system finishes booting. See
[RECEIVE\_BOOT\_COMPLETED](https://developer.android.com/reference/android/Manifest.permission#RECEIVE_BOOT_COMPLETED).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/receive\_mms**
`🔗<class_EditorExportPlatformAndroid_property_permissions/receive_mms>`

Allows an application to monitor incoming MMS messages. See
[RECEIVE\_MMS](https://developer.android.com/reference/android/Manifest.permission#RECEIVE_MMS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/receive\_sms**
`🔗<class_EditorExportPlatformAndroid_property_permissions/receive_sms>`

Allows an application to receive SMS messages. See
[RECEIVE\_SMS](https://developer.android.com/reference/android/Manifest.permission#RECEIVE_SMS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/receive\_wap\_push**
`🔗<class_EditorExportPlatformAndroid_property_permissions/receive_wap_push>`

Allows an application to receive WAP push messages. See
[RECEIVE\_WAP\_PUSH](https://developer.android.com/reference/android/Manifest.permission#RECEIVE_WAP_PUSH).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/record\_audio**
`🔗<class_EditorExportPlatformAndroid_property_permissions/record_audio>`

Allows an application to record audio. See
[RECORD\_AUDIO](https://developer.android.com/reference/android/Manifest.permission#RECORD_AUDIO).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/reorder\_tasks**
`🔗<class_EditorExportPlatformAndroid_property_permissions/reorder_tasks>`

Allows an application to change the Z-order of tasks. See
[REORDER\_TASKS](https://developer.android.com/reference/android/Manifest.permission#REORDER_TASKS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/restart\_packages**
`🔗<class_EditorExportPlatformAndroid_property_permissions/restart_packages>`

**Deprecated:** Deprecated in API level 15.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/send\_respond\_via\_message**
`🔗<class_EditorExportPlatformAndroid_property_permissions/send_respond_via_message>`

Allows an application (Phone) to send a request to other applications to
handle the respond-via-message action during incoming calls. See
[SEND\_RESPOND\_VIA\_MESSAGE](https://developer.android.com/reference/android/Manifest.permission#SEND_RESPOND_VIA_MESSAGE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/send\_sms**
`🔗<class_EditorExportPlatformAndroid_property_permissions/send_sms>`

Allows an application to send SMS messages. See
[SEND\_SMS](https://developer.android.com/reference/android/Manifest.permission#SEND_SMS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_activity\_watcher**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_activity_watcher>`

Allows an application to watch and control how activities are started
globally in the system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_alarm**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_alarm>`

Allows an application to broadcast an Intent to set an alarm for the
user. See
[SET\_ALARM](https://developer.android.com/reference/android/Manifest.permission#SET_ALARM).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_always\_finish**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_always_finish>`

Allows an application to control whether activities are immediately
finished when put in the background. See
[SET\_ALWAYS\_FINISH](https://developer.android.com/reference/android/Manifest.permission#SET_ALWAYS_FINISH).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_animation\_scale**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_animation_scale>`

Allows to modify the global animation scaling factor. See
[SET\_ANIMATION\_SCALE](https://developer.android.com/reference/android/Manifest.permission#SET_ANIMATION_SCALE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_debug\_app**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_debug_app>`

Configure an application for debugging. See
[SET\_DEBUG\_APP](https://developer.android.com/reference/android/Manifest.permission#SET_DEBUG_APP).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_orientation**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_orientation>`

Allows low-level access to setting the orientation (actually rotation)
of the screen.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_pointer\_speed**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_pointer_speed>`

Allows low-level access to setting the pointer speed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_preferred\_applications**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_preferred_applications>`

**Deprecated:** Deprecated in API level 15.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_process\_limit**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_process_limit>`

Allows an application to set the maximum number of (not needed)
application processes that can be running. See
[SET\_PROCESS\_LIMIT](https://developer.android.com/reference/android/Manifest.permission#SET_PROCESS_LIMIT).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_time**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_time>`

Allows applications to set the system time directly. See
[SET\_TIME](https://developer.android.com/reference/android/Manifest.permission#SET_TIME).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_time\_zone**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_time_zone>`

Allows applications to set the system time zone directly. See
[SET\_TIME\_ZONE](https://developer.android.com/reference/android/Manifest.permission#SET_TIME_ZONE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_wallpaper**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_wallpaper>`

Allows applications to set the wallpaper. See
[SET\_WALLPAPER](https://developer.android.com/reference/android/Manifest.permission#SET_WALLPAPER).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/set\_wallpaper\_hints**
`🔗<class_EditorExportPlatformAndroid_property_permissions/set_wallpaper_hints>`

Allows applications to set the wallpaper hints. See
[SET\_WALLPAPER\_HINTS](https://developer.android.com/reference/android/Manifest.permission#SET_WALLPAPER_HINTS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/signal\_persistent\_processes**
`🔗<class_EditorExportPlatformAndroid_property_permissions/signal_persistent_processes>`

Allow an application to request that a signal be sent to all persistent
processes. See
[SIGNAL\_PERSISTENT\_PROCESSES](https://developer.android.com/reference/android/Manifest.permission#SIGNAL_PERSISTENT_PROCESSES).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/status\_bar**
`🔗<class_EditorExportPlatformAndroid_property_permissions/status_bar>`

Allows an application to open, close, or disable the status bar and its
icons. See
[STATUS\_BAR](https://developer.android.com/reference/android/Manifest.permission#STATUS_BAR).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/subscribed\_feeds\_read**
`🔗<class_EditorExportPlatformAndroid_property_permissions/subscribed_feeds_read>`

Allows an application to allow access the subscribed feeds
ContentProvider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/subscribed\_feeds\_write**
`🔗<class_EditorExportPlatformAndroid_property_permissions/subscribed_feeds_write>`

**Deprecated:** This property may be changed or removed in future
versions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/system\_alert\_window**
`🔗<class_EditorExportPlatformAndroid_property_permissions/system_alert_window>`

Allows an app to create windows using the type
WindowManager.LayoutParams.TYPE\_APPLICATION\_OVERLAY, shown on top of
all other apps. See
[SYSTEM\_ALERT\_WINDOW](https://developer.android.com/reference/android/Manifest.permission#SYSTEM_ALERT_WINDOW).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/transmit\_ir**
`🔗<class_EditorExportPlatformAndroid_property_permissions/transmit_ir>`

Allows using the device's IR transmitter, if available. See
[TRANSMIT\_IR](https://developer.android.com/reference/android/Manifest.permission#TRANSMIT_IR).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/uninstall\_shortcut**
`🔗<class_EditorExportPlatformAndroid_property_permissions/uninstall_shortcut>`

**Deprecated:** This property may be changed or removed in future
versions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/update\_device\_stats**
`🔗<class_EditorExportPlatformAndroid_property_permissions/update_device_stats>`

Allows an application to update device statistics. See
[UPDATE\_DEVICE\_STATS](https://developer.android.com/reference/android/Manifest.permission#UPDATE_DEVICE_STATS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/use\_credentials**
`🔗<class_EditorExportPlatformAndroid_property_permissions/use_credentials>`

Allows an application to request authtokens from the AccountManager.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/use\_sip**
`🔗<class_EditorExportPlatformAndroid_property_permissions/use_sip>`

Allows an application to use SIP service. See
[USE\_SIP](https://developer.android.com/reference/android/Manifest.permission#USE_SIP).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/vibrate**
`🔗<class_EditorExportPlatformAndroid_property_permissions/vibrate>`

Allows access to the vibrator. See
[VIBRATE](https://developer.android.com/reference/android/Manifest.permission#VIBRATE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/wake\_lock**
`🔗<class_EditorExportPlatformAndroid_property_permissions/wake_lock>`

Allows using PowerManager WakeLocks to keep processor from sleeping or
screen from dimming. See
[WAKE\_LOCK](https://developer.android.com/reference/android/Manifest.permission#WAKE_LOCK).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_apn\_settings**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_apn_settings>`

Allows applications to write the apn settings and read sensitive fields
of an existing apn settings like user and password. See
[WRITE\_APN\_SETTINGS](https://developer.android.com/reference/android/Manifest.permission#WRITE_APN_SETTINGS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_calendar**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_calendar>`

Allows an application to write the user's calendar data. See
[WRITE\_CALENDAR](https://developer.android.com/reference/android/Manifest.permission#WRITE_CALENDAR).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_call\_log**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_call_log>`

Allows an application to write (but not read) the user's call log data.
See
[WRITE\_CALL\_LOG](https://developer.android.com/reference/android/Manifest.permission#WRITE_CALL_LOG).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_contacts**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_contacts>`

Allows an application to write the user's contacts data. See
[WRITE\_CONTACTS](https://developer.android.com/reference/android/Manifest.permission#WRITE_CONTACTS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_external\_storage**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_external_storage>`

Allows an application to write to external storage. See
[WRITE\_EXTERNAL\_STORAGE](https://developer.android.com/reference/android/Manifest.permission#WRITE_EXTERNAL_STORAGE).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_gservices**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_gservices>`

Allows an application to modify the Google service map. See
[WRITE\_GSERVICES](https://developer.android.com/reference/android/Manifest.permission#WRITE_GSERVICES).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_history\_bookmarks**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_history_bookmarks>`

Allows an application to write (but not read) the user's browsing
history and bookmarks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_profile**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_profile>`

Allows an application to write (but not read) the user's personal
profile data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_secure\_settings**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_secure_settings>`

Allows an application to read or write the secure system settings. See
[WRITE\_SECURE\_SETTINGS](https://developer.android.com/reference/android/Manifest.permission#WRITE_SECURE_SETTINGS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_settings**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_settings>`

Allows an application to read or write the system settings. See
[WRITE\_SETTINGS](https://developer.android.com/reference/android/Manifest.permission#WRITE_SETTINGS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_sms**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_sms>`

Allows an application to write SMS messages.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_social\_stream**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_social_stream>`

Allows an application to write (but not read) the user's social stream
data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_sync\_settings**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_sync_settings>`

Allows applications to write the sync settings. See
[WRITE\_SYNC\_SETTINGS](https://developer.android.com/reference/android/Manifest.permission#WRITE_SYNC_SETTINGS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **permissions/write\_user\_dictionary**
`🔗<class_EditorExportPlatformAndroid_property_permissions/write_user_dictionary>`

Allows an application to write to the user dictionary.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **screen/immersive\_mode**
`🔗<class_EditorExportPlatformAndroid_property_screen/immersive_mode>`

If `true`, hides navigation and status bar.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **screen/support\_large**
`🔗<class_EditorExportPlatformAndroid_property_screen/support_large>`

Indicates whether the application supports larger screen form-factors.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **screen/support\_normal**
`🔗<class_EditorExportPlatformAndroid_property_screen/support_normal>`

Indicates whether an application supports the "normal" screen
form-factors.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **screen/support\_small**
`🔗<class_EditorExportPlatformAndroid_property_screen/support_small>`

Indicates whether the application supports smaller screen form-factors.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **screen/support\_xlarge**
`🔗<class_EditorExportPlatformAndroid_property_screen/support_xlarge>`

Indicates whether the application supports extra large screen
form-factors.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **user\_data\_backup/allow**
`🔗<class_EditorExportPlatformAndroid_property_user_data_backup/allow>`

If `true`, allows the application to participate in the backup and
restore infrastructure.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **version/code**
`🔗<class_EditorExportPlatformAndroid_property_version/code>`

Machine-readable application version. This must be incremented for every
new release pushed to the Play Store.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **version/name**
`🔗<class_EditorExportPlatformAndroid_property_version/name>`

Application version visible to the user. Falls back to
`ProjectSettings.application/config/version<class_ProjectSettings_property_application/config/version>`
if left empty.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **xr\_features/xr\_mode**
`🔗<class_EditorExportPlatformAndroid_property_xr_features/xr_mode>`

The extended reality (XR) mode for this application.
