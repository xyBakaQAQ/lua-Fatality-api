# checkbox

This type represents a checkbox control.

> ####
>
> This type inherits [`control`](https://lua.fatality.win/control.html) type. All of its base methods and fields are also available in this type.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs the checkbox.

Arguments

| Name | Type                                                     | Description |
| ---- | -------------------------------------------------------- | ----------- |
| `id` | [`control_id`](https://lua.fatality.win/control-id.html) | ID.         |

Returns

| Type       | Description        |
| ---------- | ------------------ |
| `checkbox` | Checkbox instance. |

Example

```
local cb = gui.checkbox(gui.control_id('my_id'));
```

### get\_value﻿ <a href="#get-value" id="get-value"></a>

Method

Returns checkbox' value.

Arguments

None.

Returns

| Type                                                             | Description |
| ---------------------------------------------------------------- | ----------- |
| [`value_param<bool>`](https://lua.fatality.win/value-param.html) | Value data. |

Example

```
local val = cb:get_value():get();
```

### set\_value﻿ <a href="#set-value" id="set-value"></a>

Method

Sets checkbox' value.

> ####
>
> It is advised to use this method instead of [`value_param`](https://lua.fatality.win/value-param.html)'s [`set`](https://lua.fatality.win/value-param.html#set) method.

Arguments

| Name  | Type   | Description |
| ----- | ------ | ----------- |
| `val` | `bool` | New value.  |

Returns

Nothing.

Example

```
cb:set_value(true);
```
