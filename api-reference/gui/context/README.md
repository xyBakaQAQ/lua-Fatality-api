# context

This type represents the GUI context.

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
local some_cb = ctx:find('some_cb');
```

### user﻿ <a href="#user" id="user"></a>

Field

Type: [`user_t`](https://lua.fatality.win/user-t.html)

User's basic information.
