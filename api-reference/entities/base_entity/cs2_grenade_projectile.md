# cs2\_grenade\_projectile

This type represents a grenade projectile.

> ####
>
> This type inherits [`base_entity`](https://lua.fatality.win/base-entity.html) type. All of its base methods and fields are also available in this type.

### get\_abs\_origin﻿ <a href="#get-abs-origin" id="get-abs-origin"></a>

Method

Returns the absolute origin (the one that is used for rendering).

Arguments

None.

Returns

| Type                                             | Description |
| ------------------------------------------------ | ----------- |
| [`vector`](https://lua.fatality.win/vector.html) | Origin.     |

Example

```
local org = wep:get_abs_origin();
```

### get\_grenade\_type﻿ <a href="#get-grenade-type" id="get-grenade-type"></a>

Method

Returns the grenade type.

Arguments

None.

Returns

| Type  | Description   |
| ----- | ------------- |
| `int` | Grenade type. |

Example

```
local type = gren:get_grenade_type();
```
