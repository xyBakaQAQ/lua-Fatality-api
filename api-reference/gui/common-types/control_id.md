# control\_id

This type represents a control ID.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs the ID structure.

Arguments

| Name | Type     | Description |
| ---- | -------- | ----------- |
| `id` | `string` | ID.         |

Returns

| Type         | Description   |
| ------------ | ------------- |
| `control_id` | ID structure. |

Example

```
local id = gui.control_id('my_id');
```

### id﻿ <a href="#id" id="id"></a>

FieldRead Only

Type: `int`

Hashed representation of the ID.

### id\_string﻿ <a href="#id-string" id="id-string"></a>

FieldRead Only

Type: `string`

Normal representation of the ID.
