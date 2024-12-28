# cs2\_weapon\_base\_gun

This type represents a `CCSWeaponBaseGun` class.

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

### get\_max\_speed﻿ <a href="#get-max-speed" id="get-max-speed"></a>

Method

Returns the maximal player speed when holding this weapon.

Arguments

None.

Returns

| Type    | Description        |
| ------- | ------------------ |
| `float` | Max speed, in UPS. |

Example

```
local spd = wep:get_max_speed();
```

### get\_inaccuracy﻿ <a href="#get-inaccuracy" id="get-inaccuracy"></a>

Method

Returns the current inaccuracy value.

Arguments

| Name   | Type                                                           | Description  |
| ------ | -------------------------------------------------------------- | ------------ |
| `mode` | [`csweapon_mode`](https://lua.fatality.win/csweapon-mode.html) | Weapon mode. |

Returns

| Type    | Description       |
| ------- | ----------------- |
| `float` | Inaccuracy value. |

Example

```
local inacc = wep:get_inaccuracy(csweapon_mode.primary_mode);
```

### get\_spread﻿ <a href="#get-spread" id="get-spread"></a>

Method

Returns the current spread value.

Arguments

| Name   | Type                                                           | Description  |
| ------ | -------------------------------------------------------------- | ------------ |
| `mode` | [`csweapon_mode`](https://lua.fatality.win/csweapon-mode.html) | Weapon mode. |

Returns

| Type    | Description       |
| ------- | ----------------- |
| `float` | Inaccuracy value. |

Example

```
local spread = wep:get_spread(csweapon_mode.primary_mode);
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

### is\_gun﻿ <a href="#is-gun" id="is-gun"></a>

Method

Returns `true` if this weapon is a firearm.

Arguments

None.

Returns

| Type   | Description          |
| ------ | -------------------- |
| `bool` | `true` if a firearm. |

Example

```
if wep:is_gun() then
    -- ...
end
```

### is\_attackable﻿ <a href="#is-attackable" id="is-attackable"></a>

Method

Returns `true` if you can attack with this weapon.

Arguments

None.

Returns

| Type   | Description           |
| ------ | --------------------- |
| `bool` | `true` if can attack. |

Example

```
if wep:is_attackable() then
    -- ...
end
```

### has\_secondary\_attack﻿ <a href="#has-secondary-attack" id="has-secondary-attack"></a>

Method

Returns `true` if this weapon has a secondary attack mode.

Arguments

None.

Returns

| Type   | Description                              |
| ------ | ---------------------------------------- |
| `bool` | `true` if has the secondary attack mode. |

Example

```
if wep:has_secondary_attack() then
    -- ...
end
```

### has\_spread﻿ <a href="#has-spread" id="has-spread"></a>

Method

Returns `true` if this weapon has spread (e.g. knives do not have any spread).

Arguments

None.

Returns

| Type   | Description           |
| ------ | --------------------- |
| `bool` | `true` if has spread. |

Example

```
if wep:has_spread() then
    -- ...
end
```
