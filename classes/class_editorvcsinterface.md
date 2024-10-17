github\_url  
hide

# EditorVCSInterface

**Inherits:** `Object<class_Object>`

Version Control System (VCS) interface, which reads and writes to the
local VCS in use.

classref-introduction-group

## Description

Defines the API that the editor uses to extract information from the
underlying VCS. The implementation of this API is included in VCS
plugins, which are GDExtension plugins that inherit
**EditorVCSInterface** and are attached (on demand) to the singleton
instance of **EditorVCSInterface**. Instead of performing the task
themselves, all the virtual functions listed below are calling the
internally overridden functions in the VCS plugins to provide a
plug-n-play experience. A custom VCS plugin is supposed to inherit from
**EditorVCSInterface** and override each of these virtual functions.

classref-introduction-group

## Tutorials

-   `Version control systems <../tutorials/best_practices/version_control_systems>`

classref-reftable-group

## Methods

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ChangeType**: `🔗<enum_EditorVCSInterface_ChangeType>`

classref-enumeration-constant

`ChangeType<enum_EditorVCSInterface_ChangeType>` **CHANGE\_TYPE\_NEW** =
`0`

A new file has been added.

classref-enumeration-constant

`ChangeType<enum_EditorVCSInterface_ChangeType>`
**CHANGE\_TYPE\_MODIFIED** = `1`

An earlier added file has been modified.

classref-enumeration-constant

`ChangeType<enum_EditorVCSInterface_ChangeType>`
**CHANGE\_TYPE\_RENAMED** = `2`

An earlier added file has been renamed.

classref-enumeration-constant

`ChangeType<enum_EditorVCSInterface_ChangeType>`
**CHANGE\_TYPE\_DELETED** = `3`

An earlier added file has been deleted.

classref-enumeration-constant

`ChangeType<enum_EditorVCSInterface_ChangeType>`
**CHANGE\_TYPE\_TYPECHANGE** = `4`

An earlier added file has been typechanged.

classref-enumeration-constant

`ChangeType<enum_EditorVCSInterface_ChangeType>`
**CHANGE\_TYPE\_UNMERGED** = `5`

A file is left unmerged.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TreeArea**: `🔗<enum_EditorVCSInterface_TreeArea>`

classref-enumeration-constant

`TreeArea<enum_EditorVCSInterface_TreeArea>` **TREE\_AREA\_COMMIT** =
`0`

A commit is encountered from the commit area.

classref-enumeration-constant

`TreeArea<enum_EditorVCSInterface_TreeArea>` **TREE\_AREA\_STAGED** =
`1`

A file is encountered from the staged area.

classref-enumeration-constant

`TreeArea<enum_EditorVCSInterface_TreeArea>` **TREE\_AREA\_UNSTAGED** =
`2`

A file is encountered from the unstaged area.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_checkout\_branch**(branch\_name:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__checkout_branch>`

Checks out a `branch_name` in the VCS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_commit**(msg: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__commit>`

Commits the currently staged changes and applies the commit `msg` to the
resulting commit.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_create\_branch**(branch\_name:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__create_branch>`

Creates a new branch named `branch_name` in the VCS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_create\_remote**(remote\_name:
`String<class_String>`, remote\_url: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__create_remote>`

Creates a new remote destination with name `remote_name` and points it
to `remote_url`. This can be an HTTPS remote or an SSH remote.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_discard\_file**(file\_path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__discard_file>`

Discards the changes made in a file present at `file_path`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_fetch**(remote: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__fetch>`

Fetches new changes from the `remote`, but doesn't write changes to the
current working directory. Equivalent to `git fetch`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`String<class_String>`\] **\_get\_branch\_list**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_branch_list>`

Gets an instance of an `Array<class_Array>` of `String<class_String>`s
containing available branch names in the VCS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_current\_branch\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_current_branch_name>`

Gets the current branch name defined in the VCS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_diff**(identifier: `String<class_String>`, area:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_diff>`

Returns an array of `Dictionary<class_Dictionary>` items (see
`create_diff_file<class_EditorVCSInterface_method_create_diff_file>`,
`create_diff_hunk<class_EditorVCSInterface_method_create_diff_hunk>`,
`create_diff_line<class_EditorVCSInterface_method_create_diff_line>`,
`add_line_diffs_into_diff_hunk<class_EditorVCSInterface_method_add_line_diffs_into_diff_hunk>`
and
`add_diff_hunks_into_diff_file<class_EditorVCSInterface_method_add_diff_hunks_into_diff_file>`),
each containing information about a diff. If `identifier` is a file
path, returns a file diff, and if it is a commit identifier, then
returns a commit diff.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_line\_diff**(file\_path: `String<class_String>`, text:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_line_diff>`

Returns an `Array<class_Array>` of `Dictionary<class_Dictionary>` items
(see
`create_diff_hunk<class_EditorVCSInterface_method_create_diff_hunk>`),
each containing a line diff between a file at `file_path` and the `text`
which is passed in.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_modified\_files\_data**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_modified_files_data>`

Returns an `Array<class_Array>` of `Dictionary<class_Dictionary>` items
(see
`create_status_file<class_EditorVCSInterface_method_create_status_file>`),
each containing the status data of every modified file in the project
folder.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_previous\_commits**(max\_commits: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_previous_commits>`

Returns an `Array<class_Array>` of `Dictionary<class_Dictionary>` items
(see `create_commit<class_EditorVCSInterface_method_create_commit>`),
each containing the data for a past commit.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`String<class_String>`\] **\_get\_remotes**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_remotes>`

Returns an `Array<class_Array>` of `String<class_String>`s, each
containing the name of a remote configured in the VCS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_vcs\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__get_vcs_name>`

Returns the name of the underlying VCS provider.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_initialize**(project\_path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__initialize>`

Initializes the VCS plugin when called from the editor. Returns whether
or not the plugin was successfully initialized. A VCS project is
initialized at `project_path`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_pull**(remote: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__pull>`

Pulls changes from the remote. This can give rise to merge conflicts.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_push**(remote: `String<class_String>`,
force: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__push>`

Pushes changes to the `remote`. If `force` is `true`, a force push will
override the change history already present on the remote.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_remove\_branch**(branch\_name:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__remove_branch>`

Remove a branch from the local VCS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_remove\_remote**(remote\_name:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__remove_remote>`

Remove a remote from the local VCS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_credentials**(username:
`String<class_String>`, password: `String<class_String>`,
ssh\_public\_key\_path: `String<class_String>`, ssh\_private\_key\_path:
`String<class_String>`, ssh\_passphrase: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__set_credentials>`

Set user credentials in the underlying VCS. `username` and `password`
are used only during HTTPS authentication unless not already mentioned
in the remote URL. `ssh_public_key_path`, `ssh_private_key_path`, and
`ssh_passphrase` are only used during SSH authentication.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shut\_down**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__shut_down>`

Shuts down VCS plugin instance. Called when the user either closes the
editor or shuts down the VCS plugin through the editor UI.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_stage\_file**(file\_path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__stage_file>`

Stages the file present at `file_path` to the staged area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_unstage\_file**(file\_path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorVCSInterface_private_method__unstage_file>`

Unstages the file present at `file_path` from the staged area to the
unstaged area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**add\_diff\_hunks\_into\_diff\_file**(diff\_file:
`Dictionary<class_Dictionary>`, diff\_hunks:
`Array<class_Array>`\[`Dictionary<class_Dictionary>`\])
`🔗<class_EditorVCSInterface_method_add_diff_hunks_into_diff_file>`

Helper function to add an array of `diff_hunks` into a `diff_file`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**add\_line\_diffs\_into\_diff\_hunk**(diff\_hunk:
`Dictionary<class_Dictionary>`, line\_diffs:
`Array<class_Array>`\[`Dictionary<class_Dictionary>`\])
`🔗<class_EditorVCSInterface_method_add_line_diffs_into_diff_hunk>`

Helper function to add an array of `line_diffs` into a `diff_hunk`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **create\_commit**(msg:
`String<class_String>`, author: `String<class_String>`, id:
`String<class_String>`, unix\_timestamp: `int<class_int>`,
offset\_minutes: `int<class_int>`)
`🔗<class_EditorVCSInterface_method_create_commit>`

Helper function to create a commit `Dictionary<class_Dictionary>` item.
`msg` is the commit message of the commit. `author` is a single
human-readable string containing all the author's details, e.g. the
email and name configured in the VCS. `id` is the identifier of the
commit, in whichever format your VCS may provide an identifier to
commits. `unix_timestamp` is the UTC Unix timestamp of when the commit
was created. `offset_minutes` is the timezone offset in minutes,
recorded from the system timezone where the commit was created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **create\_diff\_file**(new\_file:
`String<class_String>`, old\_file: `String<class_String>`)
`🔗<class_EditorVCSInterface_method_create_diff_file>`

Helper function to create a `Dictionary<class_Dictionary>` for storing
old and new diff file paths.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **create\_diff\_hunk**(old\_start:
`int<class_int>`, new\_start: `int<class_int>`, old\_lines:
`int<class_int>`, new\_lines: `int<class_int>`)
`🔗<class_EditorVCSInterface_method_create_diff_hunk>`

Helper function to create a `Dictionary<class_Dictionary>` for storing
diff hunk data. `old_start` is the starting line number in old file.
`new_start` is the starting line number in new file. `old_lines` is the
number of lines in the old file. `new_lines` is the number of lines in
the new file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **create\_diff\_line**(new\_line\_no:
`int<class_int>`, old\_line\_no: `int<class_int>`, content:
`String<class_String>`, status: `String<class_String>`)
`🔗<class_EditorVCSInterface_method_create_diff_line>`

Helper function to create a `Dictionary<class_Dictionary>` for storing a
line diff. `new_line_no` is the line number in the new file (can be `-1`
if the line is deleted). `old_line_no` is the line number in the old
file (can be `-1` if the line is added). `content` is the diff text.
`status` is a single character string which stores the line origin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **create\_status\_file**(file\_path:
`String<class_String>`, change\_type:
`ChangeType<enum_EditorVCSInterface_ChangeType>`, area:
`TreeArea<enum_EditorVCSInterface_TreeArea>`)
`🔗<class_EditorVCSInterface_method_create_status_file>`

Helper function to create a `Dictionary<class_Dictionary>` used by
editor to read the status of a file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_error**(msg: `String<class_String>`)
`🔗<class_EditorVCSInterface_method_popup_error>`

Pops up an error message in the editor which is shown as coming from the
underlying VCS. Use this to show VCS specific error messages.
