# OpenXR body tracking

Support for full body tracking in OpenXR is only just becoming available
for a select few platforms. As support solidifies information will be
added to this page.

## HTC Tracker support

An option that has been available for some time is doing full body
tracking using HTC trackers. These are currently supported through
SteamVR and on HTC Elite XR headsets. They are exposed through the
action map system.

These trackers are identified by their roles which are assigned to them
when configured. Simply add `XRController3D <class_xrcontroller3d>`
nodes as children to the `XROrigin3D <class_xrorigin3d>` node and assign
one of the following trackers:

<table>
<caption>HTC trackers</caption>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr>
<td>/user/vive_tracker_htcx/role/handheld_object</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/left_foot</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/right_foot</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/left_shoulder</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/right_shoulder</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/left_elbow</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/right_elbow</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/left_knee</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/right_knee</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/waist</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/chest</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/camera</td>
</tr>
<tr>
<td>/user/vive_tracker_htcx/role/keyboard</td>
</tr>
</tbody>
</table>

You can now use these as targets for IK modifiers on a full body avatar.
