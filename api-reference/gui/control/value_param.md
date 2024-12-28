# value\_param

This type represents a value data used by some control types.

> ####
>
> Note, that this part: `<type>` is used to designate what exact type the instance of this type is holding. For example, when it says `value_param<bool>`, it means that `get` will return a `bool` value, and `set` will accept only the type `bool` as it's `val` parameter.

### get﻿ <a href="#get" id="get"></a>

Method

Returns the value.

Arguments

None.

Returns

| Type     | Description |
| -------- | ----------- |
| `<type>` | Value.      |

Example

```
ctrl:get_value():get();
```

### set﻿ <a href="#set" id="set"></a>

Method

Sets the value.

> ####
>
> It is advised to use `set_value` method of the control, if any.

Arguments

| Name  | Type     | Description |
| ----- | -------- | ----------- |
| `val` | `<type>` | Value.      |

Returns

Nothing.

Example

```
ctrl:get_value():set(123);
```

### get\_hotkey\_state﻿ <a href="#get-hotkey-state" id="get-hotkey-state"></a>

Method

Returns `true` if there's any active hotkeys.

Arguments

None.

Returns

| Type   | Description                     |
| ------ | ------------------------------- |
| `bool` | `true` if any hotkey is active. |

Example

```
if ctrl:get_value():get_hotkey_state() then
    -- ...
end
```

### disable\_hotkeys﻿ <a href="#disable-hotkeys" id="disable-hotkeys"></a>

Method

Disables all active hotkeys. This allows you to override the value.

Arguments

None.

Returns

Nothing.

Example

```
ctrl:get_value():disable_hotkeys();
```
