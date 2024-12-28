# container

This type represents an abstract container.

### add﻿ <a href="#add" id="add"></a>

Method

Adds a control to the container.

Arguments

| Name   | Type                                               | Description     |
| ------ | -------------------------------------------------- | --------------- |
| `ctrl` | [`control`](https://lua.fatality.win/control.html) | Control to add. |

Returns

Nothing.

Example

```
container:add(my_control);
```

### remove﻿ <a href="#remove" id="remove"></a>

Method

Removes a control from the container.

Arguments

| Name   | Type                                               | Description        |
| ------ | -------------------------------------------------- | ------------------ |
| `ctrl` | [`control`](https://lua.fatality.win/control.html) | Control to remove. |

Returns

Nothing.

Example

```
container:remove(my_control);
```

### find﻿ <a href="#find" id="find"></a>

Method

Finds a control by ID.

Arguments

| Name | Type     | Description |
| ---- | -------- | ----------- |
| `id` | `string` | Control ID. |

Returns

| Type         | Description                                                                    |
| ------------ | ------------------------------------------------------------------------------ |
| `<control>?` | Casted control. Returns `nil` if the control was not found, or casting failed. |

Example

```
local some_cb = container:find('some_cb');
```
