# cs2\_player\_controller

This type represents a `CCSPlayerController` class.

> ####
>
> This type inherits [`base_entity`](https://lua.fatality.win/base-entity.html) type. All of its base methods and fields are also available in this type.

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

### get\_pawn﻿ <a href="#get-pawn" id="get-pawn"></a>

Method

Returns the pawn attached to this controller.

Arguments

None.

Returns

| Type                                                               | Description    |
| ------------------------------------------------------------------ | -------------- |
| [`cs2_player_pawn`](https://lua.fatality.win/cs2-player-pawn.html) | Pawn instance. |

Example

```
local pawn = ctrl:get_pawn();
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

### get\_observer\_pawn﻿ <a href="#get-observer-pawn" id="get-observer-pawn"></a>

Method

Returns the observer pawn used for this controller.

Arguments

None.

Returns

| Type                                                       | Description |
| ---------------------------------------------------------- | ----------- |
| [`base_entity`](https://lua.fatality.win/base-entity.html) | Entity.     |

Example

```
local obs_pawn = ctrl:get_observer_pawn();
```

### get\_observer\_target﻿ <a href="#get-observer-target" id="get-observer-target"></a>

Method

Returns the pawn this controller is currently observing.

Arguments

None.

Returns

| Type                                                       | Description |
| ---------------------------------------------------------- | ----------- |
| [`base_entity`](https://lua.fatality.win/base-entity.html) | Entity.     |

Example

```
local obs = ctrl:get_observer_target();
```

### get\_observer\_mode﻿ <a href="#get-observer-mode" id="get-observer-mode"></a>

Method

Returns the current observer mode.

Arguments

None.

Returns

| Type                                                               | Description    |
| ------------------------------------------------------------------ | -------------- |
| [`observer_mode_t`](https://lua.fatality.win/observer-mode-t.html) | Observer mode. |

Example

```
local mode = ctrl:get_observer_mode();
```
