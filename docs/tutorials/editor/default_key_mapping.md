article\_outdated  
True

# Default editor shortcuts

Many Godot editor functions can be executed with keyboard shortcuts.
This page lists functions which have associated shortcuts by default,
but many others are available for customization in editor settings as
well. To change keys associated with these and other actions navigate to
**Editor &gt; Editor Settings &gt; Shortcuts**.

While some actions are universal, a lot of shortcuts are specific to
individual tools. For this reason it is possible for some key
combinations to be assigned to more than one function. The correct
action will be performed depending on the context.

Note

While Windows and Linux builds of the editor share most of the default
settings, some shortcuts may differ for macOS version. This is done for
better integration of the editor into macOS ecosystem. Users fluent with
standard shortcuts on that OS should find Godot Editor's default key
mapping intuitive.

## General editor actions

<table style="width:98%;">
<colgroup>
<col style="width: 19%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 28%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Open 2D Editor</td>
<td><code class="interpreted-text" role="kbd">Ctrl + F1</code></td>
<td><code class="interpreted-text" role="kbd">Opt + 1</code></td>
<td><code>editor/editor_2d</code></td>
</tr>
<tr>
<td>Open 3D Editor</td>
<td><code class="interpreted-text" role="kbd">Ctrl + F2</code></td>
<td><code class="interpreted-text" role="kbd">Opt + 2</code></td>
<td><code>editor/editor_3d</code></td>
</tr>
<tr>
<td>Open Script Editor</td>
<td><code class="interpreted-text" role="kbd">Ctrl + F3</code></td>
<td><code class="interpreted-text" role="kbd">Opt + 3</code></td>
<td><code>editor/editor_script</code></td>
</tr>
<tr>
<td>Search Help</td>
<td><code class="interpreted-text" role="kbd">F1</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Space</code></td>
<td><code>editor/editor_help</code></td>
</tr>
<tr>
<td>Distraction Free Mode</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + F11</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Ctrl + D</code></td>
<td><code>editor/distraction_free_mode</code></td>
</tr>
<tr>
<td>Next tab</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Tab</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Tab</code></td>
<td><code>editor/next_tab</code></td>
</tr>
<tr>
<td>Previous tab</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + Tab</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + Tab</code></td>
<td><code>editor/prev_tab</code></td>
</tr>
<tr>
<td>Filter Files</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + P</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + P</code></td>
<td><code>editor/filter_files</code></td>
</tr>
<tr>
<td>Open Scene</td>
<td><code class="interpreted-text" role="kbd">Ctrl + O</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + O</code></td>
<td><code>editor/open_scene</code></td>
</tr>
<tr>
<td>Close Scene</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + W</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + W</code></td>
<td><code>editor/close_scene</code></td>
</tr>
<tr>
<td>Reopen Closed Scene</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + T</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + T</code></td>
<td><code>editor/reopen_closed_scene</code></td>
</tr>
<tr>
<td>Save Scene</td>
<td><code class="interpreted-text" role="kbd">Ctrl + S</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + S</code></td>
<td><code>editor/save_scene</code></td>
</tr>
<tr>
<td>Save Scene As</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + S</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + S</code></td>
<td><code>editor/save_scene_as</code></td>
</tr>
<tr>
<td>Save All Scenes</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + Alt + S</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + Opt + S</code></td>
<td><code>editor/save_all_scenes</code></td>
</tr>
<tr>
<td>Quick Open</td>
<td><code class="interpreted-text"
role="kbd">Shift + Alt + O</code></td>
<td><code class="interpreted-text"
role="kbd">Shift + Opt + O</code></td>
<td><code>editor/quick_open</code></td>
</tr>
<tr>
<td>Quick Open Scene</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + O</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + O</code></td>
<td><code>editor/quick_open_scene</code></td>
</tr>
<tr>
<td>Quick Open Script</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + O</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + O</code></td>
<td><code>editor/quick_open_script</code></td>
</tr>
<tr>
<td>Undo</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Z</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Z</code></td>
<td><code>editor/undo</code></td>
</tr>
<tr>
<td>Redo</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + Z</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + Z</code></td>
<td><code>editor/redo</code></td>
</tr>
<tr>
<td>Quit</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Q</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Q</code></td>
<td><code>editor/file_quit</code></td>
</tr>
<tr>
<td>Quit to Project List</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + Q</code></td>
<td><code class="interpreted-text"
role="kbd">Shift + Opt + Q</code></td>
<td><code>editor/quit_to_project_list</code></td>
</tr>
<tr>
<td>Take Screenshot</td>
<td><code class="interpreted-text" role="kbd">Ctrl + F12</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + F12</code></td>
<td><code>editor/take_screenshot</code></td>
</tr>
<tr>
<td>Toggle Fullscreen</td>
<td><code class="interpreted-text" role="kbd">Shift + F11</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Ctrl + F</code></td>
<td><code>editor/fullscreen_mode</code></td>
</tr>
<tr>
<td>Play</td>
<td><code class="interpreted-text" role="kbd">F5</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + B</code></td>
<td><code>editor/play</code></td>
</tr>
<tr>
<td>Pause Scene</td>
<td><code class="interpreted-text" role="kbd">F7</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Ctrl + Y</code></td>
<td><code>editor/pause_scene</code></td>
</tr>
<tr>
<td>Stop</td>
<td><code class="interpreted-text" role="kbd">F8</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + .</code></td>
<td><code>editor/stop</code></td>
</tr>
<tr>
<td>Play Scene</td>
<td><code class="interpreted-text" role="kbd">F6</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + R</code></td>
<td><code>editor/play_scene</code></td>
</tr>
<tr>
<td>Play Custom Scene</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + F5</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + R</code></td>
<td><code>editor/play_custom_scene</code></td>
</tr>
<tr>
<td>Expand Bottom Panel</td>
<td><code class="interpreted-text" role="kbd">Shift + F12</code></td>
<td><code class="interpreted-text" role="kbd">Shift + F12</code></td>
<td><code>editor/bottom_panel_expand</code></td>
</tr>
<tr>
<td>Command Palette</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + P</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + P</code></td>
<td><code>editor/command_palette</code></td>
</tr>
</tbody>
</table>

## Bottom panels

Only bottom panels that are always available have a default shortcut
assigned. Others must be manually bound in the Editor Settings if
desired.

<table style="width:98%;">
<colgroup>
<col style="width: 28%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 42%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Toggle Last Opened Panel</td>
<td><code class="interpreted-text" role="kbd">Ctrl + J</code></td>
<td><code class="interpreted-text" role="kbd">Ctrl + J</code></td>
<td><code>editor/toggle_last_opened_bottom_panel</code></td>
</tr>
<tr>
<td>Toggle Animation Bottom Panel</td>
<td><code class="interpreted-text" role="kbd">Alt + N</code></td>
<td><code class="interpreted-text" role="kbd">Alt + N</code></td>
<td><code>bottom_panels/toggle_animation_bottom_panel</code></td>
</tr>
<tr>
<td>Toggle Audio Bottom Panel</td>
<td><code class="interpreted-text" role="kbd">Alt + A</code></td>
<td><code class="interpreted-text" role="kbd">Alt + A</code></td>
<td><code>bottom_panels/toggle_audio_bottom_panel</code></td>
</tr>
<tr>
<td>Toggle Debugger Bottom Panel</td>
<td><code class="interpreted-text" role="kbd">Alt + D</code></td>
<td><code class="interpreted-text" role="kbd">Alt + D</code></td>
<td><code>bottom_panels/toggle_debugger_bottom_panel</code></td>
</tr>
<tr>
<td>Toggle FileSystem Bottom Panel</td>
<td><code class="interpreted-text" role="kbd">Alt + F</code></td>
<td><code class="interpreted-text" role="kbd">Alt + F</code></td>
<td><code>bottom_panels/toggle_filesystem_bottom_panel</code></td>
</tr>
<tr>
<td>Toggle Output Bottom Panel</td>
<td><code class="interpreted-text" role="kbd">Alt + O</code></td>
<td><code class="interpreted-text" role="kbd">Alt + O</code></td>
<td><code>bottom_panels/toggle_output_bottom_panel</code></td>
</tr>
<tr>
<td>Toggle Shader Editor Bottom Panel</td>
<td><code class="interpreted-text" role="kbd">Alt + S</code></td>
<td><code class="interpreted-text" role="kbd">Alt + S</code></td>
<td><code>bottom_panels/toggle_shader_editor_bottom_panel</code></td>
</tr>
</tbody>
</table>

## 2D / CanvasItem editor

<table style="width:99%;">
<colgroup>
<col style="width: 21%" />
<col style="width: 18%" />
<col style="width: 17%" />
<col style="width: 40%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Zoom In</td>
<td><code class="interpreted-text" role="kbd">Ctrl + =</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + =</code></td>
<td><code>canvas_item_editor/zoom_plus</code></td>
</tr>
<tr>
<td>Zoom Out</td>
<td><code class="interpreted-text" role="kbd">Ctrl + -</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + -</code></td>
<td><code>canvas_item_editor/zoom_minus</code></td>
</tr>
<tr>
<td>Zoom Reset</td>
<td><code class="interpreted-text" role="kbd">Ctrl + 0</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + 0</code></td>
<td><code>canvas_item_editor/zoom_reset</code></td>
</tr>
<tr>
<td>Pan View</td>
<td><code class="interpreted-text" role="kbd">Space</code></td>
<td><code class="interpreted-text" role="kbd">Space</code></td>
<td><code>canvas_item_editor/pan_view</code></td>
</tr>
<tr>
<td>Select Mode</td>
<td><code class="interpreted-text" role="kbd">Q</code></td>
<td><code class="interpreted-text" role="kbd">Q</code></td>
<td><code>canvas_item_editor/select_mode</code></td>
</tr>
<tr>
<td>Move Mode</td>
<td><code class="interpreted-text" role="kbd">W</code></td>
<td><code class="interpreted-text" role="kbd">W</code></td>
<td><code>canvas_item_editor/move_mode</code></td>
</tr>
<tr>
<td>Rotate Mode</td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code>canvas_item_editor/rotate_mode</code></td>
</tr>
<tr>
<td>Scale Mode</td>
<td><code class="interpreted-text" role="kbd">S</code></td>
<td><code class="interpreted-text" role="kbd">S</code></td>
<td><code>canvas_item_editor/scale_mode</code></td>
</tr>
<tr>
<td>Ruler Mode</td>
<td><code class="interpreted-text" role="kbd">R</code></td>
<td><code class="interpreted-text" role="kbd">R</code></td>
<td><code>canvas_item_editor/ruler_mode</code></td>
</tr>
<tr>
<td>Use Smart Snap</td>
<td><code class="interpreted-text" role="kbd">Shift + S</code></td>
<td><code class="interpreted-text" role="kbd">Shift + S</code></td>
<td><code>canvas_item_editor/use_smart_snap</code></td>
</tr>
<tr>
<td>Use Grid Snap</td>
<td><code class="interpreted-text" role="kbd">Shift + G</code></td>
<td><code class="interpreted-text" role="kbd">Shift + G</code></td>
<td><code>canvas_item_editor/use_grid_snap</code></td>
</tr>
<tr>
<td>Multiply grid step by 2</td>
<td><code class="interpreted-text" role="kbd">Num *</code></td>
<td><code class="interpreted-text" role="kbd">Num *</code></td>
<td><code>canvas_item_editor/multiply_grid_step</code></td>
</tr>
<tr>
<td>Divide grid step by 2</td>
<td><code class="interpreted-text" role="kbd">Num /</code></td>
<td><code class="interpreted-text" role="kbd">Num /</code></td>
<td><code>canvas_item_editor/divide_grid_step</code></td>
</tr>
<tr>
<td>Always Show Grid</td>
<td><code class="interpreted-text" role="kbd">G</code></td>
<td><code class="interpreted-text" role="kbd">G</code></td>
<td><code>canvas_item_editor/show_grid</code></td>
</tr>
<tr>
<td>Show Helpers</td>
<td><code class="interpreted-text" role="kbd">H</code></td>
<td><code class="interpreted-text" role="kbd">H</code></td>
<td><code>canvas_item_editor/show_helpers</code></td>
</tr>
<tr>
<td>Show Guides</td>
<td><code class="interpreted-text" role="kbd">Y</code></td>
<td><code class="interpreted-text" role="kbd">Y</code></td>
<td><code>canvas_item_editor/show_guides</code></td>
</tr>
<tr>
<td>Center Selection</td>
<td><code class="interpreted-text" role="kbd">F</code></td>
<td><code class="interpreted-text" role="kbd">F</code></td>
<td><code>canvas_item_editor/center_selection</code></td>
</tr>
<tr>
<td>Frame Selection</td>
<td><code class="interpreted-text" role="kbd">Shift + F</code></td>
<td><code class="interpreted-text" role="kbd">Shift + F</code></td>
<td><code>canvas_item_editor/frame_selection</code></td>
</tr>
<tr>
<td>Preview Canvas Scale</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + P</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + P</code></td>
<td><code>canvas_item_editor/preview_canvas_scale</code></td>
</tr>
<tr>
<td>Insert Key</td>
<td><code class="interpreted-text" role="kbd">Ins</code></td>
<td><code class="interpreted-text" role="kbd">Ins</code></td>
<td><code>canvas_item_editor/anim_insert_key</code></td>
</tr>
<tr>
<td>Insert Key (Existing Tracks)</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Ins</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Ins</code></td>
<td><code>canvas_item_editor/anim_insert_key_existing_tracks</code></td>
</tr>
<tr>
<td>Make Custom Bones from Nodes</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + B</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + B</code></td>
<td><code>canvas_item_editor/skeleton_make_bones</code></td>
</tr>
<tr>
<td>Clear Pose</td>
<td><code class="interpreted-text" role="kbd">Shift + K</code></td>
<td><code class="interpreted-text" role="kbd">Shift + K</code></td>
<td><code>canvas_item_editor/anim_clear_pose</code></td>
</tr>
</tbody>
</table>

## 3D / Spatial editor

<table style="width:99%;">
<colgroup>
<col style="width: 27%" />
<col style="width: 17%" />
<col style="width: 16%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Toggle Freelook</td>
<td><code class="interpreted-text" role="kbd">Shift + F</code></td>
<td><code class="interpreted-text" role="kbd">Shift + F</code></td>
<td><code>spatial_editor/freelook_toggle</code></td>
</tr>
<tr>
<td>Freelook Left</td>
<td><code class="interpreted-text" role="kbd">A</code></td>
<td><code class="interpreted-text" role="kbd">A</code></td>
<td><code>spatial_editor/freelook_left</code></td>
</tr>
<tr>
<td>Freelook Right</td>
<td><code class="interpreted-text" role="kbd">D</code></td>
<td><code class="interpreted-text" role="kbd">D</code></td>
<td><code>spatial_editor/freelook_right</code></td>
</tr>
<tr>
<td>Freelook Forward</td>
<td><code class="interpreted-text" role="kbd">W</code></td>
<td><code class="interpreted-text" role="kbd">W</code></td>
<td><code>spatial_editor/freelook_forward</code></td>
</tr>
<tr>
<td>Freelook Backwards</td>
<td><code class="interpreted-text" role="kbd">S</code></td>
<td><code class="interpreted-text" role="kbd">S</code></td>
<td><code>spatial_editor/freelook_backwards</code></td>
</tr>
<tr>
<td>Freelook Up</td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code>spatial_editor/freelook_up</code></td>
</tr>
<tr>
<td>Freelook Down</td>
<td><code class="interpreted-text" role="kbd">Q</code></td>
<td><code class="interpreted-text" role="kbd">Q</code></td>
<td><code>spatial_editor/freelook_down</code></td>
</tr>
<tr>
<td>Freelook Speed Modifier</td>
<td><code class="interpreted-text" role="kbd">Shift</code></td>
<td><code class="interpreted-text" role="kbd">Shift</code></td>
<td><code>spatial_editor/freelook_speed_modifier</code></td>
</tr>
<tr>
<td>Freelook Slow Modifier</td>
<td><code class="interpreted-text" role="kbd">Alt</code></td>
<td><code class="interpreted-text" role="kbd">Opt</code></td>
<td><code>spatial_editor/freelook_slow_modifier</code></td>
</tr>
<tr>
<td>Select Mode</td>
<td><code class="interpreted-text" role="kbd">Q</code></td>
<td><code class="interpreted-text" role="kbd">Q</code></td>
<td><code>spatial_editor/tool_select</code></td>
</tr>
<tr>
<td>Move Mode</td>
<td><code class="interpreted-text" role="kbd">W</code></td>
<td><code class="interpreted-text" role="kbd">W</code></td>
<td><code>spatial_editor/tool_move</code></td>
</tr>
<tr>
<td>Rotate Mode</td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code>spatial_editor/tool_rotate</code></td>
</tr>
<tr>
<td>Scale Mode</td>
<td><code class="interpreted-text" role="kbd">R</code></td>
<td><code class="interpreted-text" role="kbd">R</code></td>
<td><code>spatial_editor/tool_scale</code></td>
</tr>
<tr>
<td>Use Local Space</td>
<td><code class="interpreted-text" role="kbd">T</code></td>
<td><code class="interpreted-text" role="kbd">T</code></td>
<td><code>spatial_editor/local_coords</code></td>
</tr>
<tr>
<td>Use Snap</td>
<td><code class="interpreted-text" role="kbd">Y</code></td>
<td><code class="interpreted-text" role="kbd">Y</code></td>
<td><code>spatial_editor/snap</code></td>
</tr>
<tr>
<td>Snap Object to Floor</td>
<td><code class="interpreted-text" role="kbd">PgDown</code></td>
<td><code class="interpreted-text" role="kbd">PgDown</code></td>
<td><code>spatial_editor/snap_to_floor</code></td>
</tr>
<tr>
<td>Top View</td>
<td><code class="interpreted-text" role="kbd">Num 7</code></td>
<td><code class="interpreted-text" role="kbd">Num 7</code></td>
<td><code>spatial_editor/top_view</code></td>
</tr>
<tr>
<td>Bottom View</td>
<td><code class="interpreted-text" role="kbd">Alt + Num 7</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Num 7</code></td>
<td><code>spatial_editor/bottom_view</code></td>
</tr>
<tr>
<td>Front View</td>
<td><code class="interpreted-text" role="kbd">Num 1</code></td>
<td><code class="interpreted-text" role="kbd">Num 1</code></td>
<td><code>spatial_editor/front_view</code></td>
</tr>
<tr>
<td>Rear View</td>
<td><code class="interpreted-text" role="kbd">Alt + Num 1</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Num 1</code></td>
<td><code>spatial_editor/rear_view</code></td>
</tr>
<tr>
<td>Right View</td>
<td><code class="interpreted-text" role="kbd">Num 3</code></td>
<td><code class="interpreted-text" role="kbd">Num 3</code></td>
<td><code>spatial_editor/right_view</code></td>
</tr>
<tr>
<td>Left View</td>
<td><code class="interpreted-text" role="kbd">Alt + Num 3</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Num 3</code></td>
<td><code>spatial_editor/left_view</code></td>
</tr>
<tr>
<td>Switch Perspective/Orthogonal View</td>
<td><code class="interpreted-text" role="kbd">Num 5</code></td>
<td><code class="interpreted-text" role="kbd">Num 5</code></td>
<td><code>spatial_editor/switch_perspective_orthogonal</code></td>
</tr>
<tr>
<td>Insert Animation Key</td>
<td><code class="interpreted-text" role="kbd">K</code></td>
<td><code class="interpreted-text" role="kbd">K</code></td>
<td><code>spatial_editor/insert_anim_key</code></td>
</tr>
<tr>
<td>Focus Origin</td>
<td><code class="interpreted-text" role="kbd">O</code></td>
<td><code class="interpreted-text" role="kbd">O</code></td>
<td><code>spatial_editor/focus_origin</code></td>
</tr>
<tr>
<td>Focus Selection</td>
<td><code class="interpreted-text" role="kbd">F</code></td>
<td><code class="interpreted-text" role="kbd">F</code></td>
<td><code>spatial_editor/focus_selection</code></td>
</tr>
<tr>
<td>Align Transform with View</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + M</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + M</code></td>
<td><code>spatial_editor/align_transform_with_view</code></td>
</tr>
<tr>
<td>Align Rotation with View</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + F</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + F</code></td>
<td><code>spatial_editor/align_rotation_with_view</code></td>
</tr>
<tr>
<td>1 Viewport</td>
<td><code class="interpreted-text" role="kbd">Ctrl + 1</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + 1</code></td>
<td><code>spatial_editor/1_viewport</code></td>
</tr>
<tr>
<td>2 Viewports</td>
<td><code class="interpreted-text" role="kbd">Ctrl + 2</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + 2</code></td>
<td><code>spatial_editor/2_viewports</code></td>
</tr>
<tr>
<td>2 Viewports (Alt)</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + 2</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + 2</code></td>
<td><code>spatial_editor/2_viewports_alt</code></td>
</tr>
<tr>
<td>3 Viewports</td>
<td><code class="interpreted-text" role="kbd">Ctrl + 3</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + 3</code></td>
<td><code>spatial_editor/3_viewports</code></td>
</tr>
<tr>
<td>3 Viewports (Alt)</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + 3</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + 3</code></td>
<td><code>spatial_editor/3_viewports_alt</code></td>
</tr>
<tr>
<td>4 Viewports</td>
<td><code class="interpreted-text" role="kbd">Ctrl + 4</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + 4</code></td>
<td><code>spatial_editor/4_viewports</code></td>
</tr>
</tbody>
</table>

## Text editor

<table style="width:99%;">
<colgroup>
<col style="width: 18%" />
<col style="width: 22%" />
<col style="width: 23%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Cut</td>
<td><code class="interpreted-text" role="kbd">Ctrl + X</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + X</code></td>
<td><code>script_text_editor/cut</code></td>
</tr>
<tr>
<td>Copy</td>
<td><code class="interpreted-text" role="kbd">Ctrl + C</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + C</code></td>
<td><code>script_text_editor/copy</code></td>
</tr>
<tr>
<td>Paste</td>
<td><code class="interpreted-text" role="kbd">Ctrl + V</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + V</code></td>
<td><code>script_text_editor/paste</code></td>
</tr>
<tr>
<td>Select All</td>
<td><code class="interpreted-text" role="kbd">Ctrl + A</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + A</code></td>
<td><code>script_text_editor/select_all</code></td>
</tr>
<tr>
<td>Find</td>
<td><code class="interpreted-text" role="kbd">Ctrl + F</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + F</code></td>
<td><code>script_text_editor/find</code></td>
</tr>
<tr>
<td>Find Next</td>
<td><code class="interpreted-text" role="kbd">F3</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + G</code></td>
<td><code>script_text_editor/find_next</code></td>
</tr>
<tr>
<td>Find Previous</td>
<td><code class="interpreted-text" role="kbd">Shift + F3</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + G</code></td>
<td><code>script_text_editor/find_previous</code></td>
</tr>
<tr>
<td>Find in Files</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + F</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + F</code></td>
<td><code>script_text_editor/find_in_files</code></td>
</tr>
<tr>
<td>Replace</td>
<td><code class="interpreted-text" role="kbd">Ctrl + R</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + F</code></td>
<td><code>script_text_editor/replace</code></td>
</tr>
<tr>
<td>Replace in Files</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + R</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + R</code></td>
<td><code>script_text_editor/replace_in_files</code></td>
</tr>
<tr>
<td>Undo</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Z</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Z</code></td>
<td><code>script_text_editor/undo</code></td>
</tr>
<tr>
<td>Redo</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Y</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Y</code></td>
<td><code>script_text_editor/redo</code></td>
</tr>
<tr>
<td>Move Up</td>
<td><code class="interpreted-text" role="kbd">Alt + Up Arrow</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Up Arrow</code></td>
<td><code>script_text_editor/move_up</code></td>
</tr>
<tr>
<td>Move Down</td>
<td><code class="interpreted-text"
role="kbd">Alt + Down Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Opt + Down Arrow</code></td>
<td><code>script_text_editor/move_down</code></td>
</tr>
<tr>
<td>Delete Line</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + K</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + K</code></td>
<td><code>script_text_editor/delete_line</code></td>
</tr>
<tr>
<td>Toggle Comment</td>
<td><code class="interpreted-text" role="kbd">Ctrl + K</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + K</code></td>
<td><code>script_text_editor/toggle_comment</code></td>
</tr>
<tr>
<td>Fold/Unfold Line</td>
<td><code class="interpreted-text" role="kbd">Alt + F</code></td>
<td><code class="interpreted-text" role="kbd">Ctrl + Cmd + F</code></td>
<td><code>script_text_editor/toggle_fold_line</code></td>
</tr>
<tr>
<td>Duplicate Lines</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Alt + Down Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + Down Arrow</code></td>
<td><code>script_text_editor/duplicate_lines</code></td>
</tr>
<tr>
<td>Duplicate Selection</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + D</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + C</code></td>
<td><code>script_text_editor/duplicate_selection</code></td>
</tr>
<tr>
<td>Complete Symbol</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Space</code></td>
<td><code class="interpreted-text" role="kbd">Ctrl + Space</code></td>
<td><code>script_text_editor/complete_symbol</code></td>
</tr>
<tr>
<td>Evaluate Selection</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + E</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + E</code></td>
<td><code>script_text_editor/evaluate_selection</code></td>
</tr>
<tr>
<td>Trim Trailing Whitespace</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + T</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + T</code></td>
<td><code>script_text_editor/trim_trailing_whitespace</code></td>
</tr>
<tr>
<td>Uppercase</td>
<td><code class="interpreted-text" role="kbd">Shift + F4</code></td>
<td><code class="interpreted-text" role="kbd">Shift + F4</code></td>
<td><code>script_text_editor/convert_to_uppercase</code></td>
</tr>
<tr>
<td>Lowercase</td>
<td><code class="interpreted-text" role="kbd">Shift + F5</code></td>
<td><code class="interpreted-text" role="kbd">Shift + F5</code></td>
<td><code>script_text_editor/convert_to_lowercase</code></td>
</tr>
<tr>
<td>Capitalize</td>
<td><code class="interpreted-text" role="kbd">Shift + F6</code></td>
<td><code class="interpreted-text" role="kbd">Shift + F6</code></td>
<td><code>script_text_editor/capitalize</code></td>
</tr>
<tr>
<td>Convert Indent to Spaces</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + Y</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + Y</code></td>
<td><code>script_text_editor/convert_indent_to_spaces</code></td>
</tr>
<tr>
<td>Convert Indent to Tabs</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + I</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + I</code></td>
<td><code>script_text_editor/convert_indent_to_tabs</code></td>
</tr>
<tr>
<td>Auto Indent</td>
<td><code class="interpreted-text" role="kbd">Ctrl + I</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + I</code></td>
<td><code>script_text_editor/auto_indent</code></td>
</tr>
<tr>
<td>Toggle Bookmark</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + B</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + B</code></td>
<td><code>script_text_editor/toggle_bookmark</code></td>
</tr>
<tr>
<td>Go to Next Bookmark</td>
<td><code class="interpreted-text" role="kbd">Ctrl + B</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + B</code></td>
<td><code>script_text_editor/goto_next_bookmark</code></td>
</tr>
<tr>
<td>Go to Previous Bookmark</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + B</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + B</code></td>
<td><code>script_text_editor/goto_previous_bookmark</code></td>
</tr>
<tr>
<td>Go to Function</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + F</code></td>
<td><code class="interpreted-text" role="kbd">Ctrl + Cmd + J</code></td>
<td><code>script_text_editor/goto_function</code></td>
</tr>
<tr>
<td>Go to Line</td>
<td><code class="interpreted-text" role="kbd">Ctrl + L</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + L</code></td>
<td><code>script_text_editor/goto_line</code></td>
</tr>
<tr>
<td>Toggle Breakpoint</td>
<td><code class="interpreted-text" role="kbd">F9</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + B</code></td>
<td><code>script_text_editor/toggle_breakpoint</code></td>
</tr>
<tr>
<td>Remove All Breakpoints</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + F9</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + F9</code></td>
<td><code>script_text_editor/remove_all_breakpoints</code></td>
</tr>
<tr>
<td>Go to Next Breakpoint</td>
<td><code class="interpreted-text" role="kbd">Ctrl + .</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + .</code></td>
<td><code>script_text_editor/goto_next_breakpoint</code></td>
</tr>
<tr>
<td>Go to Previous Breakpoint</td>
<td><code class="interpreted-text" role="kbd">Ctrl + ,</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + ,</code></td>
<td><code>script_text_editor/goto_previous_breakpoint</code></td>
</tr>
<tr>
<td>Contextual Help</td>
<td><code class="interpreted-text" role="kbd">Alt + F1</code></td>
<td><code class="interpreted-text"
role="kbd">Opt + Shift + Space</code></td>
<td><code>script_text_editor/contextual_help</code></td>
</tr>
</tbody>
</table>

## Script editor

<table style="width:99%;">
<colgroup>
<col style="width: 17%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 30%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Find</td>
<td><code class="interpreted-text" role="kbd">Ctrl + F</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + F</code></td>
<td><code>script_editor/find</code></td>
</tr>
<tr>
<td>Find Next</td>
<td><code class="interpreted-text" role="kbd">F3</code></td>
<td><code class="interpreted-text" role="kbd">F3</code></td>
<td><code>script_editor/find_next</code></td>
</tr>
<tr>
<td>Find Previous</td>
<td><code class="interpreted-text" role="kbd">Shift + F3</code></td>
<td><code class="interpreted-text" role="kbd">Shift + F3</code></td>
<td><code>script_editor/find_previous</code></td>
</tr>
<tr>
<td>Find in Files</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + F</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + F</code></td>
<td><code>script_editor/find_in_files</code></td>
</tr>
<tr>
<td>Move Up</td>
<td><code class="interpreted-text"
role="kbd">Shift + Alt + Up Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Shift + Opt + Up Arrow</code></td>
<td><code>script_editor/window_move_up</code></td>
</tr>
<tr>
<td>Move Down</td>
<td><code class="interpreted-text"
role="kbd">Shift + Alt + Down Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Shift + Opt + Down Arrow</code></td>
<td><code>script_editor/window_move_down</code></td>
</tr>
<tr>
<td>Next Script</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + .</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + .</code></td>
<td><code>script_editor/next_script</code></td>
</tr>
<tr>
<td>Previous Script</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + ,</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + ,</code></td>
<td><code>script_editor/prev_script</code></td>
</tr>
<tr>
<td>Reopen Closed Script</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + T</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + T</code></td>
<td><code>script_editor/reopen_closed_script</code></td>
</tr>
<tr>
<td>Save</td>
<td><code class="interpreted-text" role="kbd">Ctrl + Alt + S</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Cmd + S</code></td>
<td><code>script_editor/save</code></td>
</tr>
<tr>
<td>Save All</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + Alt + S</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + Opt + S</code></td>
<td><code>script_editor/save_all</code></td>
</tr>
<tr>
<td>Soft Reload Script</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + R</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + R</code></td>
<td><code>script_editor/reload_script_soft</code></td>
</tr>
<tr>
<td>History Previous</td>
<td><code class="interpreted-text"
role="kbd">Alt + Left Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Opt + Left Arrow</code></td>
<td><code>script_editor/history_previous</code></td>
</tr>
<tr>
<td>History Next</td>
<td><code class="interpreted-text"
role="kbd">Alt + Right Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Opt + Right Arrow</code></td>
<td><code>script_editor/history_next</code></td>
</tr>
<tr>
<td>Close</td>
<td><code class="interpreted-text" role="kbd">Ctrl + W</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + W</code></td>
<td><code>script_editor/close_file</code></td>
</tr>
<tr>
<td>Run</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + X</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + X</code></td>
<td><code>script_editor/run_file</code></td>
</tr>
<tr>
<td>Toggle Scripts Panel</td>
<td><code class="interpreted-text" role="kbd">Ctrl + \\</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + \\</code></td>
<td><code>script_editor/toggle_scripts_panel</code></td>
</tr>
<tr>
<td>Zoom In</td>
<td><code class="interpreted-text" role="kbd">Ctrl + =</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + =</code></td>
<td><code>script_editor/zoom_in</code></td>
</tr>
<tr>
<td>Zoom Out</td>
<td><code class="interpreted-text" role="kbd">Ctrl + -</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + -</code></td>
<td><code>script_editor/zoom_out</code></td>
</tr>
<tr>
<td>Reset Zoom</td>
<td><code class="interpreted-text" role="kbd">Ctrl + 0</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + 0</code></td>
<td><code>script_editor/reset_zoom</code></td>
</tr>
</tbody>
</table>

## Editor output

<table style="width:98%;">
<colgroup>
<col style="width: 17%" />
<col style="width: 27%" />
<col style="width: 26%" />
<col style="width: 27%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Copy Selection</td>
<td><code class="interpreted-text" role="kbd">Ctrl + C</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + C</code></td>
<td><code>editor/copy_output</code></td>
</tr>
<tr>
<td>Clear Output</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + K</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + K</code></td>
<td><code>editor/clear_output</code></td>
</tr>
</tbody>
</table>

## Debugger

<table style="width:96%;">
<colgroup>
<col style="width: 19%" />
<col style="width: 23%" />
<col style="width: 18%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Step Into</td>
<td><code class="interpreted-text" role="kbd">F11</code></td>
<td><code class="interpreted-text" role="kbd">F11</code></td>
<td><code>debugger/step_into</code></td>
</tr>
<tr>
<td>Step Over</td>
<td><code class="interpreted-text" role="kbd">F10</code></td>
<td><code class="interpreted-text" role="kbd">F10</code></td>
<td><code>debugger/step_over</code></td>
</tr>
<tr>
<td>Continue</td>
<td><code class="interpreted-text" role="kbd">F12</code></td>
<td><code class="interpreted-text" role="kbd">F12</code></td>
<td><code>debugger/continue</code></td>
</tr>
</tbody>
</table>

## File dialog

<table style="width:98%;">
<colgroup>
<col style="width: 18%" />
<col style="width: 23%" />
<col style="width: 23%" />
<col style="width: 32%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Go Back</td>
<td><code class="interpreted-text"
role="kbd">Alt + Left Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Opt + Left Arrow</code></td>
<td><code>file_dialog/go_back</code></td>
</tr>
<tr>
<td>Go Forward</td>
<td><code class="interpreted-text"
role="kbd">Alt + Right Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Opt + Right Arrow</code></td>
<td><code>file_dialog/go_forward</code></td>
</tr>
<tr>
<td>Go Up</td>
<td><code class="interpreted-text" role="kbd">Alt + Up Arrow</code></td>
<td><code class="interpreted-text" role="kbd">Opt + Up Arrow</code></td>
<td><code>file_dialog/go_up</code></td>
</tr>
<tr>
<td>Refresh</td>
<td><code class="interpreted-text" role="kbd">F5</code></td>
<td><code class="interpreted-text" role="kbd">F5</code></td>
<td><code>file_dialog/refresh</code></td>
</tr>
<tr>
<td>Toggle Hidden Files</td>
<td><code class="interpreted-text" role="kbd">Ctrl + H</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + H</code></td>
<td><code>file_dialog/toggle_hidden_files</code></td>
</tr>
<tr>
<td>Toggle Favorite</td>
<td><code class="interpreted-text" role="kbd">Alt + F</code></td>
<td><code class="interpreted-text" role="kbd">Opt + F</code></td>
<td><code>file_dialog/toggle_favorite</code></td>
</tr>
<tr>
<td>Toggle Mode</td>
<td><code class="interpreted-text" role="kbd">Alt + V</code></td>
<td><code class="interpreted-text" role="kbd">Opt + V</code></td>
<td><code>file_dialog/toggle_mode</code></td>
</tr>
<tr>
<td>Create Folder</td>
<td><code class="interpreted-text" role="kbd">Ctrl + N</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + N</code></td>
<td><code>file_dialog/create_folder</code></td>
</tr>
<tr>
<td>Delete</td>
<td><code class="interpreted-text" role="kbd">Del</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + BkSp</code></td>
<td><code>file_dialog/delete</code></td>
</tr>
<tr>
<td>Focus Path</td>
<td><code class="interpreted-text" role="kbd">Ctrl + L</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + G</code></td>
<td><code>file_dialog/focus_path</code></td>
</tr>
<tr>
<td>Move Favorite Up</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Up Arrow</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Up Arrow</code></td>
<td><code>file_dialog/move_favorite_up</code></td>
</tr>
<tr>
<td>Move Favorite Down</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Down Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Down Arrow</code></td>
<td><code>file_dialog/move_favorite_down</code></td>
</tr>
</tbody>
</table>

## FileSystem dock

<table style="width:98%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 20%" />
<col style="width: 23%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Copy Path</td>
<td><code class="interpreted-text" role="kbd">Ctrl + C</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + C</code></td>
<td><code>filesystem_dock/copy_path</code></td>
</tr>
<tr>
<td>Duplicate</td>
<td><code class="interpreted-text" role="kbd">Ctrl + D</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + D</code></td>
<td><code>filesystem_dock/duplicate</code></td>
</tr>
<tr>
<td>Delete</td>
<td><code class="interpreted-text" role="kbd">Del</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + BkSp</code></td>
<td><code>filesystem_dock/delete</code></td>
</tr>
</tbody>
</table>

## Scene tree dock

<table style="width:98%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 25%" />
<col style="width: 24%" />
<col style="width: 32%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Add Child Node</td>
<td><code class="interpreted-text" role="kbd">Ctrl + A</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + A</code></td>
<td><code>scene_tree/add_child_node</code></td>
</tr>
<tr>
<td>Batch Rename</td>
<td><code class="interpreted-text" role="kbd">Ctrl + F2</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + F2</code></td>
<td><code>scene_tree/batch_rename</code></td>
</tr>
<tr>
<td>Copy Node Path</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + C</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift +  C</code></td>
<td><code>scene_tree/copy_node_path</code></td>
</tr>
<tr>
<td>Delete</td>
<td><code class="interpreted-text" role="kbd">Del</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + BkSp</code></td>
<td><code>scene_tree/delete</code></td>
</tr>
<tr>
<td>Force Delete</td>
<td><code class="interpreted-text" role="kbd">Shift + Del</code></td>
<td><code class="interpreted-text" role="kbd">Shift + Del</code></td>
<td><code>scene_tree/delete_no_confirm</code></td>
</tr>
<tr>
<td>Duplicate</td>
<td><code class="interpreted-text" role="kbd">Ctrl + D</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + D</code></td>
<td><code>scene_tree/duplicate</code></td>
</tr>
<tr>
<td>Move Up</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Up Arrow</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + Up Arrow</code></td>
<td><code>scene_tree/move_up</code></td>
</tr>
<tr>
<td>Move Down</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Down Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Down Arrow</code></td>
<td><code>scene_tree/move_down</code></td>
</tr>
</tbody>
</table>

## Animation track editor

<table style="width:99%;">
<colgroup>
<col style="width: 17%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 40%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Duplicate Selection</td>
<td><code class="interpreted-text" role="kbd">Ctrl + D</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + D</code></td>
<td><code>animation_editor/duplicate_selection</code></td>
</tr>
<tr>
<td>Duplicate Transposed</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Shift + D</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Shift + D</code></td>
<td><code>animation_editor/duplicate_selection_transposed</code></td>
</tr>
<tr>
<td>Delete Selection</td>
<td><code class="interpreted-text" role="kbd">Del</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + BkSp</code></td>
<td><code>animation_editor/delete_selection</code></td>
</tr>
<tr>
<td>Go to Next Step</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Right Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Right Arrow</code></td>
<td><code>animation_editor/goto_next_step</code></td>
</tr>
<tr>
<td>Go to Previous Step</td>
<td><code class="interpreted-text"
role="kbd">Ctrl + Left Arrow</code></td>
<td><code class="interpreted-text"
role="kbd">Cmd + Left Arrow</code></td>
<td><code>animation_editor/goto_prev_step</code></td>
</tr>
</tbody>
</table>

## TileMap editor

<table style="width:98%;">
<colgroup>
<col style="width: 20%" />
<col style="width: 18%" />
<col style="width: 20%" />
<col style="width: 40%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Select</td>
<td><code class="interpreted-text" role="kbd">S</code></td>
<td><code class="interpreted-text" role="kbd">S</code></td>
<td><code>tiles_editor/selection_tool</code></td>
</tr>
<tr>
<td>Cut Selection</td>
<td><code class="interpreted-text" role="kbd">Ctrl + X</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + X</code></td>
<td><code>tiles_editor/cut</code></td>
</tr>
<tr>
<td>Copy Selection</td>
<td><code class="interpreted-text" role="kbd">Ctrl + C</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + C</code></td>
<td><code>tiles_editor/copy</code></td>
</tr>
<tr>
<td>Paste Selection</td>
<td><code class="interpreted-text" role="kbd">Ctrl + V</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + V</code></td>
<td><code>tiles_editor/paste</code></td>
</tr>
<tr>
<td>Delete Selection</td>
<td><code class="interpreted-text" role="kbd">Del</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + BkSp</code></td>
<td><code>tiles_editor/delete</code></td>
</tr>
<tr>
<td>Cancel</td>
<td><code class="interpreted-text" role="kbd">Esc</code></td>
<td><code class="interpreted-text" role="kbd">Esc</code></td>
<td><code>tiles_editor/cancel</code></td>
</tr>
<tr>
<td>Paint</td>
<td><code class="interpreted-text" role="kbd">D</code></td>
<td><code class="interpreted-text" role="kbd">D</code></td>
<td><code>tiles_editor/paint_tool</code></td>
</tr>
<tr>
<td>Line</td>
<td><code class="interpreted-text" role="kbd">L</code></td>
<td><code class="interpreted-text" role="kbd">L</code></td>
<td><code>tiles_editor/line_tool</code></td>
</tr>
<tr>
<td>Rect</td>
<td><code class="interpreted-text" role="kbd">R</code></td>
<td><code class="interpreted-text" role="kbd">R</code></td>
<td><code>tiles_editor/rect_tool</code></td>
</tr>
<tr>
<td>Bucket</td>
<td><code class="interpreted-text" role="kbd">B</code></td>
<td><code class="interpreted-text" role="kbd">B</code></td>
<td><code>tiles_editor/bucket_tool</code></td>
</tr>
<tr>
<td>Picker</td>
<td><code class="interpreted-text" role="kbd">P</code></td>
<td><code class="interpreted-text" role="kbd">P</code></td>
<td><code>tiles_editor/picker</code></td>
</tr>
<tr>
<td>Eraser</td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code class="interpreted-text" role="kbd">E</code></td>
<td><code>tiles_editor/eraser</code></td>
</tr>
<tr>
<td>Flip Horizontally</td>
<td><code class="interpreted-text" role="kbd">C</code></td>
<td><code class="interpreted-text" role="kbd">C</code></td>
<td><code>tiles_editor/flip_tile_horizontal</code></td>
</tr>
<tr>
<td>Flip Vertically</td>
<td><code class="interpreted-text" role="kbd">V</code></td>
<td><code class="interpreted-text" role="kbd">V</code></td>
<td><code>tiles_editor/flip_tile_vertical</code></td>
</tr>
<tr>
<td>Rotate Left</td>
<td><code class="interpreted-text" role="kbd">Z</code></td>
<td><code class="interpreted-text" role="kbd">Z</code></td>
<td><code>tiles_editor/rotate_tile_left</code></td>
</tr>
<tr>
<td>Rotate Right</td>
<td><code class="interpreted-text" role="kbd">X</code></td>
<td><code class="interpreted-text" role="kbd">X</code></td>
<td><code>tiles_editor/rotate_tile_right</code></td>
</tr>
</tbody>
</table>

## TileSet Editor

<table style="width:98%;">
<colgroup>
<col style="width: 22%" />
<col style="width: 17%" />
<col style="width: 16%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>Next Coordinate</td>
<td><code class="interpreted-text" role="kbd">PgDown</code></td>
<td><code class="interpreted-text" role="kbd">PgDown</code></td>
<td><code>tileset_editor/next_shape</code></td>
</tr>
<tr>
<td>Previous Coordinate</td>
<td><code class="interpreted-text" role="kbd">PgUp</code></td>
<td><code class="interpreted-text" role="kbd">PgUp</code></td>
<td><code>tileset_editor/previous_shape</code></td>
</tr>
<tr>
<td>Region Mode</td>
<td><code class="interpreted-text" role="kbd">1</code></td>
<td><code class="interpreted-text" role="kbd">1</code></td>
<td><code>tileset_editor/editmode_region</code></td>
</tr>
<tr>
<td>Collision Mode</td>
<td><code class="interpreted-text" role="kbd">2</code></td>
<td><code class="interpreted-text" role="kbd">2</code></td>
<td><code>tileset_editor/editmode_collision</code></td>
</tr>
<tr>
<td>Occlusion Mode</td>
<td><code class="interpreted-text" role="kbd">3</code></td>
<td><code class="interpreted-text" role="kbd">3</code></td>
<td><code>tileset_editor/editmode_occlusion</code></td>
</tr>
<tr>
<td>Navigation Mode</td>
<td><code class="interpreted-text" role="kbd">4</code></td>
<td><code class="interpreted-text" role="kbd">4</code></td>
<td><code>tileset_editor/editmode_navigation</code></td>
</tr>
<tr>
<td>Bitmask Mode</td>
<td><code class="interpreted-text" role="kbd">5</code></td>
<td><code class="interpreted-text" role="kbd">5</code></td>
<td><code>tileset_editor/editmode_bitmask</code></td>
</tr>
<tr>
<td>Priority Mode</td>
<td><code class="interpreted-text" role="kbd">6</code></td>
<td><code class="interpreted-text" role="kbd">6</code></td>
<td><code>tileset_editor/editmode_priority</code></td>
</tr>
<tr>
<td>Icon Mode</td>
<td><code class="interpreted-text" role="kbd">7</code></td>
<td><code class="interpreted-text" role="kbd">7</code></td>
<td><code>tileset_editor/editmode_icon</code></td>
</tr>
<tr>
<td>Z Index Mode</td>
<td><code class="interpreted-text" role="kbd">8</code></td>
<td><code class="interpreted-text" role="kbd">8</code></td>
<td><code>tileset_editor/editmode_z_index</code></td>
</tr>
</tbody>
</table>

## Project manager

<table style="width:98%;">
<colgroup>
<col style="width: 22%" />
<col style="width: 18%" />
<col style="width: 20%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr>
<th>Action name</th>
<th>Windows, Linux</th>
<th>macOS</th>
<th>Editor setting</th>
</tr>
</thead>
<tbody>
<tr>
<td>New Project</td>
<td><code class="interpreted-text" role="kbd">Ctrl + N</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + N</code></td>
<td><code>project_manager/new_project</code></td>
</tr>
<tr>
<td>Import Project</td>
<td><code class="interpreted-text" role="kbd">Ctrl + I</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + I</code></td>
<td><code>project_manager/import_project</code></td>
</tr>
<tr>
<td>Scan for Projects</td>
<td><code class="interpreted-text" role="kbd">Ctrl + S</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + S</code></td>
<td><code>project_manager/scan_projects</code></td>
</tr>
<tr>
<td>Edit Project</td>
<td><code class="interpreted-text" role="kbd">Ctrl + E</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + E</code></td>
<td><code>project_manager/edit_project</code></td>
</tr>
<tr>
<td>Run Project</td>
<td><code class="interpreted-text" role="kbd">Ctrl + R</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + R</code></td>
<td><code>project_manager/run_project</code></td>
</tr>
<tr>
<td>Rename Project</td>
<td><code class="interpreted-text" role="kbd">F2</code></td>
<td><code class="interpreted-text" role="kbd">Enter</code></td>
<td><code>project_manager/rename_project</code></td>
</tr>
<tr>
<td>Remove Project</td>
<td><code class="interpreted-text" role="kbd">Delete</code></td>
<td><code class="interpreted-text" role="kbd">Cmd + BkSp</code></td>
<td><code>project_manager/remove_project</code></td>
</tr>
</tbody>
</table>
