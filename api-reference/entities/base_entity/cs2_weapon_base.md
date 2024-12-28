# cs2\_weapon\_base

This type represents a `CCSWeaponBase` entity.

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

### get\_id﻿ <a href="#get-id" id="get-id"></a>

Method

Returns the weapon ID.

Arguments

None.

Returns

| Type                                                   | Description |
| ------------------------------------------------------ | ----------- |
| [`weapon_id`](https://lua.fatality.win/weapon-id.html) | Weapon ID.  |

Example

```
local wep_id = wep:get_id();
```

### get\_type﻿ <a href="#get-type" id="get-type"></a>

Method

Returns the weapon type.

Arguments

None.

Returns

| Type                                                           | Description  |
| -------------------------------------------------------------- | ------------ |
| [`csweapon_type`](https://lua.fatality.win/csweapon-type.html) | Weapon type. |

Example

```
local type = wep:get_type();
```

### get\_data﻿ <a href="#get-data" id="get-data"></a>

Method

Returns the weapon static data.

Arguments

None.

Returns

| Type                                                                         | Description  |
| ---------------------------------------------------------------------------- | ------------ |
| [`ccsweapon_base_vdata`](https://lua.fatality.win/ccsweapon-base-vdata.html) | Weapon data. |

Example

```
local data = wep:get_data();
```
