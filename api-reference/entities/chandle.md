# chandle

This type represents an entity handle.

> ####
>
> You can also compare this type using a `==` operator.

### get﻿ <a href="#get" id="get"></a>

Method

Returns the entity, or `nil` if nothing found.

Arguments

None.

Returns

| Type     | Description      |
| -------- | ---------------- |
| `<type>` | Entity instance. |

Example

```
local ent = handle:get();
```

### valid﻿ <a href="#valid" id="valid"></a>

Method

Returns `true` if the handle is valid.

Arguments

None.

Returns

| Type   | Description      |
| ------ | ---------------- |
| `bool` | `true` if valid. |

Example

```
if handle:valid() then
    -- ...
end
```

### is\_clientside﻿ <a href="#is-clientside" id="is-clientside"></a>

Method

Returns `true` if the handle links to a client-side entity.

Arguments

None.

Returns

| Type   | Description             |
| ------ | ----------------------- |
| `bool` | `true` if client-sided. |

Example

```
if handle:is_clientside() then
    -- ...
end
```
