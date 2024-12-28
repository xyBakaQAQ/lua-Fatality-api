# schema\_accessor\_t

This type represents a special structure that references a certain field in the entity object.

> ####
>
> You can check the returned type by using `type()` function.

> ####
>
> Do not ever store an instance of this type anywhere but in a scope of an event because entity might be removed.

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
local health = player.m_iHealth:get();
```

### set﻿ <a href="#set" id="set"></a>

Method

Sets the value.

Arguments

| Name    | Type     | Description |
| ------- | -------- | ----------- |
| `value` | `<type>` | Value.      |

Returns

Nothing.

Example

```
player.m_iHealth:set(50); -- won't really do anything with the health
```
