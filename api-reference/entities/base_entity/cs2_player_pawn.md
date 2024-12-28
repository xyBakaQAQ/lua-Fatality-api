# cs2\_player\_pawn

This type represents a `C_CSPlayerPawn` class.

> ####
>
> This type inherits [`base_entity`](https://lua.fatality.win/base-entity.html) type. All of its base methods and fields are also available in this type.

### should\_draw﻿ <a href="#should-draw" id="should-draw"></a>

Method

Returns `true` if the game will draw this player on screen.

Arguments

None.

Returns

| Type   | Description     |
| ------ | --------------- |
| `bool` | `true` if will. |

Example

```
if player:should_draw() then
    -- ...
end
```

### is\_left\_handed﻿ <a href="#is-left-handed" id="is-left-handed"></a>

Method

Returns `true` if left-hand mode is enabled.

Arguments

None.

Returns

| Type   | Description            |
| ------ | ---------------------- |
| `bool` | `true` if left-handed. |

Example

```
if player:is_left_handed() then
    -- ...
end
```

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
local org = player:get_abs_origin();
```

### get\_abs\_angles﻿ <a href="#get-abs-angles" id="get-abs-angles"></a>

Method

Returns the absolute angles (the one that is used for rendering).

Arguments

None.

Returns

| Type                                             | Description |
| ------------------------------------------------ | ----------- |
| [`vector`](https://lua.fatality.win/vector.html) | Angles.     |

Example

```
local ang = player:get_abs_angles();
```

### set\_abs\_origin﻿ <a href="#set-abs-origin" id="set-abs-origin"></a>

Method

Sets the new absolute origin.

Arguments

| Name  | Type                                             | Description |
| ----- | ------------------------------------------------ | ----------- |
| `vec` | [`vector`](https://lua.fatality.win/vector.html) | New origin. |

Returns

Nothing.

Example

```
player:set_abs_origin(my_vec);
```

### set\_abs\_angles﻿ <a href="#set-abs-angles" id="set-abs-angles"></a>

Method

Sets new absolute angles.

Arguments

| Name  | Type                                             | Description |
| ----- | ------------------------------------------------ | ----------- |
| `ang` | [`vector`](https://lua.fatality.win/vector.html) | New angles. |

Returns

Nothing.

Example

```
player:set_abs_angles(my_ang);
```

### is\_alive﻿ <a href="#is-alive" id="is-alive"></a>

Method

Returns `true` if the player is alive.

Arguments

None.

Returns

| Type   | Description      |
| ------ | ---------------- |
| `bool` | `true` if alive. |

Example

```
if player:is_alive() then
    -- ...
end
```

### is\_enemy﻿ <a href="#is-enemy" id="is-enemy"></a>

Method

Returns `true` if this player is an enemy to the local player.

Arguments

None.

Returns

| Type   | Description         |
| ------ | ------------------- |
| `bool` | `true` if an enemy. |

Example

```
if player:is_enemy() then
    -- ...
end
```

### is\_enemy\_to﻿ <a href="#is-enemy-to" id="is-enemy-to"></a>

Method

Returns whether this player is an enemy to another entity.

Arguments

| Name  | Type                                                       | Description   |
| ----- | ---------------------------------------------------------- | ------------- |
| `ent` | [`base_entity`](https://lua.fatality.win/base-entity.html) | Other entity. |

Returns

| Type   | Description         |
| ------ | ------------------- |
| `bool` | `true` if an enemy. |

Example

```
if player:is_enemy_to(other_player) then
    -- ...
end
```

### get\_active\_weapon﻿ <a href="#get-active-weapon" id="get-active-weapon"></a>

Method

Returns the active weapon.

Arguments

None.

Returns

| Type                                                                       | Description      |
| -------------------------------------------------------------------------- | ---------------- |
| [`cs2_weapon_base_gun`](https://lua.fatality.win/cs2-weapon-base-gun.html) | Weapon instance. |

Example

```
local wep = player:get_active_weapon();
```

### get\_name﻿ <a href="#get-name" id="get-name"></a>

Method

Returns the sanitized player name.

Arguments

None.

Returns

| Type     | Description    |
| -------- | -------------- |
| `string` | Player's name. |

Example

```
local name = player:get_name();
```

### get\_view\_offset﻿ <a href="#get-view-offset" id="get-view-offset"></a>

Method

Returns the player's view offset (eye location relative to the player's origin).

Arguments

None.

Returns

| Type                                             | Description  |
| ------------------------------------------------ | ------------ |
| [`vector`](https://lua.fatality.win/vector.html) | View offset. |

Example

```
local vo = player:get_view_offset();
```

### get\_eye\_pos﻿ <a href="#get-eye-pos" id="get-eye-pos"></a>

Method

Returns the player's eye position.

Arguments

None.

Returns

| Type                                             | Description   |
| ------------------------------------------------ | ------------- |
| [`vector`](https://lua.fatality.win/vector.html) | Eye position. |

Example

```
local eyes = player:get_eye_pos();
```
