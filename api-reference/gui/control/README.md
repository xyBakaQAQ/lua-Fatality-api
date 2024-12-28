# control

This type represents an abstract GUI control.

### id﻿ <a href="#id" id="id"></a>

FieldRead Only

Type: `int`

Control ID.

### id\_string﻿ <a href="#id-string" id="id-string"></a>

FieldRead Only

Type: `string`

String representation of control's ID. This may be empty for some controls.

### is\_visible﻿ <a href="#is-visible" id="is-visible"></a>

FieldRead Only

Type: `bool`

Control's visibility state.

### parent﻿ <a href="#parent" id="parent"></a>

FieldRead Only

Type: `control?`

Parent control. Might be `nil` on some controls.

### type﻿ <a href="#type" id="type"></a>

FieldRead Only

Type: [`control_type`](https://lua.fatality.win/control-type.html)

Control's type.

### inactive﻿ <a href="#inactive" id="inactive"></a>

Field

Type: `bool`

If set to `true`, will mark this control to the inactive state.

### inactive\_text﻿ <a href="#inactive-text" id="inactive-text"></a>

Field

Type: `string`

Tooltip replacement to show when control is inactive.

### inactive\_color﻿ <a href="#inactive-color" id="inactive-color"></a>

Field

Type: [`color`](https://lua.fatality.win/rcolor.html)

Label color override for inactive controls.

### tooltip﻿ <a href="#tooltip" id="tooltip"></a>

Field

Type: `string`

Tooltip text.

### aliases﻿ <a href="#aliases" id="aliases"></a>

Field

Type: `table[string]`

Alias list for this control. Used in search box to support different naming (e.g. if a user searches for "Double tap", will find "Rapid fire" instead).

### get\_hotkey\_state﻿ <a href="#get-hotkey-state" id="get-hotkey-state"></a>

Method

Returns `true` if any of the control's hotkeys are active.

Arguments

None.

Returns

| Type   | Description                     |
| ------ | ------------------------------- |
| `bool` | `true` if any hotkey is active. |

Example

```
if ctrl:get_hotkey_state() then
    -- ...
end
```

### set\_visible﻿ <a href="#set-visible" id="set-visible"></a>

Method

Changes visibility state for this control.

> ####
>
> Calling this method on controls that are located in layouts with large amount of other controls will inevitably cause performance issues due to auto-stacking.

Arguments

| Name  | Type   | Description       |
| ----- | ------ | ----------------- |
| `val` | `bool` | Visibility state. |

Returns

Nothing.

Example

```
ctrl:set_visible(false);
```

### add\_callback﻿ <a href="#add-callback" id="add-callback"></a>

Method

Adds a callback to this control.

Arguments

| Name  | Type       | Description |
| ----- | ---------- | ----------- |
| `cbk` | `function` | Callback.   |

Returns

Nothing.

Example

```
ctrl:add_callback(function ()
    print('Callback invoked!');
end);
```

### cast﻿ <a href="#cast" id="cast"></a>

Method

Attempts to downcast the control to the correct type.

> ####
>
> Due to Lua engine's limitations, it is impossible to automatically downcast variables. Usually there is no need to call this method, unless you found some control that wasn't somehow already cast to the desired type. `find()` methods automatically perform the cast to the correct type.

Arguments

None.

Returns

| Type        | Description       |
| ----------- | ----------------- |
| `<control>` | New type, if any. |

Example

```
local checkbox = maybe_checkbox:cast();
```

### reset﻿ <a href="#reset" id="reset"></a>

Method

Resets control's state. This action is usually required if you change control's value directly by interacting with [`value_param`](https://lua.fatality.win/value-param.html).

Arguments

None.

Returns

Nothing.

Example

```
ctrl:reset();
```
