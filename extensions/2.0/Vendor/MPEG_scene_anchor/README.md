# MPEG_scene_anchor

## Contributors

* ISO/IEC SC29 WG3 (MPEG Systems) - Scene Description Breakout Group
* Contacts
  * Thomas Stockhammer (MPEG-I Scene Description BoG Chair, tsto@qti.qualcomm.com)

## Status

Based on [ISO/IEC FDIS 23090-14/CD Amd.2](https://www.iso.org/standard/86439.html), available as [WG03_N0797](https://mpeg.expert/live/nextcloud/index.php/s/f6prqzxWMdDM3r2)

## Dependencies

Written against the glTF 2.0 spec.

## Overview

---------------------------------------
<a name="reference-mpeg-scene-anchor-extension"></a>

## MPEG scene anchor extension

MPEG scene and node anchor is used to anchor a scene/node to the viewer's real-world environment.

**`MPEG scene anchor extension` Properties**

|   |Type|Description|Required|
|---|---|---|---|
|**trackables**|[`MPEG_scene_anchor.trackable`](#reference-mpeg_scene_anchor-trackable) `[1-*]`|An array of trackables.| &#10003; Yes|
|**anchors**|[`MPEG_scene_anchor.anchor`](#reference-mpeg_scene_anchor-anchor) `[1-*]`|An array of anchors.| &#10003; Yes|
|**extensions**|`object`|JSON object with extension-specific objects.|No|
|**extras**|[`any`](#reference-any)|Application-specific data.|No|

Additional properties are allowed.

* **JSON schema**: [MPEG_scene_anchor.schema.json](/schema/MPEG_scene_anchor.schema.json)

### MPEG scene anchor extension.trackables

An array of trackables.

* **Type**: [`MPEG_scene_anchor.trackable`](#reference-mpeg_scene_anchor-trackable) `[1-*]`
* **Required**:  &#10003; Yes

### MPEG scene anchor extension.anchors

An array of anchors.

* **Type**: [`MPEG_scene_anchor.anchor`](#reference-mpeg_scene_anchor-anchor) `[1-*]`
* **Required**:  &#10003; Yes

### MPEG scene anchor extension.extensions

JSON object with extension-specific objects.

* **Type**: `object`
* **Required**: No
* **Type of each property**: Extension

### MPEG scene anchor extension.extras

Application-specific data.

* **Type**: [`any`](#reference-any)
* **Required**: No

---------------------------------------
<a name="reference-mpeg_scene_anchor-anchor"></a>

## MPEG_scene_anchor.anchor object

anchor object.

**`MPEG_scene_anchor.anchor object` Properties**

|   |Type|Description|Required|
|---|---|---|---|
|**trackable**|`number`|| &#10003; Yes|
|**requiresAnchoring**|`boolean`|| &#10003; Yes|
|**minimumRequiredSpace**|`number` `[3]`||No|
|**aligned**|`string`||No|
|**actions**|`number` `[1-*]`|An array of associated actions.|No|
|**extensions**|[`any`](#reference-any)||No|
|**extras**|[`any`](#reference-any)||No|

Additional properties are allowed.

* **JSON schema**: [MPEG_scene_anchor.anchor.schema.json](/schema/MPEG_scene_anchor.anchor.schema.json)

### MPEG_scene_anchor.anchor.trackable

* **Type**: `number`
* **Required**:  &#10003; Yes

### MPEG_scene_anchor.anchor.requiresAnchoring

* **Type**: `boolean`
* **Required**:  &#10003; Yes

### MPEG_scene_anchor.anchor.minimumRequiredSpace

* **Type**: `number` `[3]`
* **Required**: No

### MPEG_scene_anchor.anchor.aligned

* **Type**: `string`
* **Required**: No
* **Allowed values**:
  * `"NOT_USED"`
  * `"ALIGNED_NOTSCALED"`
  * `"ALIGNED_SCALED"`

### MPEG_scene_anchor.anchor.actions

An array of associated actions.

* **Type**: `number` `[1-*]`
* **Required**: No

### MPEG_scene_anchor.anchor.extensions

* **Type**: [`any`](#reference-any)
* **Required**: No

### MPEG_scene_anchor.anchor.extras

* **Type**: [`any`](#reference-any)
* **Required**: No

---------------------------------------
<a name="reference-mpeg_scene_anchor-trackable"></a>

## MPEG_scene_anchor.trackable object

MPEG scene and node anchor is used to anchor a scene/node to the viewer's real-world environment.

**`MPEG_scene_anchor.trackable object` Properties**

|   |Type|Description|Required|
|---|---|---|---|
|**type**|`string`|the type of the trackable.| &#10003; Yes|
|**parameters**|`object`||No|
|**extensions**|`object`|JSON object with extension-specific objects.|No|
|**extras**|[`any`](#reference-any)|Application-specific data.|No|

Additional properties are allowed.

* **JSON schema**: [MPEG_scene_anchor.trackable.schema.json](/schema/MPEG_scene_anchor.trackable.schema.json)

### MPEG_scene_anchor.trackable.type

the type of the trackable.

* **Type**: `string`
* **Required**:  &#10003; Yes
* **Allowed values**:
  * `"TRACKABLE_FLOOR"`
  * `"TRACKABLE_CONTROLLER"`
  * `"TRACKABLE_GEOMETRIC"`
  * `"TRACKABLE_MARKER_2D"`
  * `"TRACKABLE_MARKER_3D"`
  * `"TRACKABLE_MARKER_GEO"`
  * `"TRACKABLE_APPLICATION"`

### MPEG_scene_anchor.trackable.parameters

* **Type**: `object`
* **Required**: No
* **Allowed values**:

### MPEG_scene_anchor.trackable.extensions

JSON object with extension-specific objects.

* **Type**: `object`
* **Required**: No
* **Type of each property**: Extension

### MPEG_scene_anchor.trackable.extras

Application-specific data.

* **Type**: [`any`](#reference-any)
* **Required**: No

## Known Implementations

* [ISO/IEC WD 23090-24](https://www.iso.org/standard/83696.html)

## Resources

* [ISO/IEC 23090-14/CD Amd 2](https://www.iso.org/standard/86439.html), Information technology — Coded representation of immersive media — Part 14: Scene description — Amendment 2: Support for haptics, augmented reality, avatars, Interactivity, MPEG-I audio, and lighting 
* [ISO/IEC WD 23090-24](https://www.iso.org/standard/83696.html), Information technology — Coded representation of immersive media — Part 24: Conformance and Reference Software for Scene Description for MPEG Media

## License

Copyright ISO/IEC 2023

The use of the "MPEG scene description extensions" is subject to the license as accessible here: https://standards.iso.org/ and is subject to the IPR policy as accessible here: https://www.iso.org/iso-standards-and-patents.html.
