# entities

This table represents an internal entity list.

> ####
>
> Never store any entities in the global scope! Any entity might get deleted, and you will no longer have a valid instance of that entity, which will inevitably lead to a crash. If you need to globally store an entity somewhere, we strongly recommend you store an instance of [`chandle`](https://lua.fatality.win/chandle.html), and use it's [`get`](https://lua.fatality.win/chandle.html#get) method to retrieve the entity again, when needed.

### players﻿ <a href="#players" id="players"></a>

Field

Type: [`entity_list_t<cs2_player_pawn>`](https://lua.fatality.win/entity-list-t.html)

Player pawns.

### controllers﻿ <a href="#controllers" id="controllers"></a>

Field

Type: [`entity_list_t<cs2_player_controller>`](https://lua.fatality.win/entity-list-t.html)

Player controllers.

### items﻿ <a href="#items" id="items"></a>

Field

Type: [`entity_list_t<cs2_weapon_base>`](https://lua.fatality.win/entity-list-t.html)

Items (held).

### dropped\_items﻿ <a href="#dropped-items" id="dropped-items"></a>

Field

Type: [`entity_list_t<cs2_weapon_base>`](https://lua.fatality.win/entity-list-t.html)

Dropped items.

### projectiles﻿ <a href="#projectiles" id="projectiles"></a>

Field

Type: [`entity_list_t<cs2_grenade_projectile>`](https://lua.fatality.win/entity-list-t.html)

Grenade projectiles.

### get\_local\_pawn﻿ <a href="#get-local-pawn" id="get-local-pawn"></a>

Function

Returns the local player's pawn.

Arguments

None.

Returns

| Type                                                               | Description |
| ------------------------------------------------------------------ | ----------- |
| [`cs2_player_pawn`](https://lua.fatality.win/cs2-player-pawn.html) | Pawn.       |

Example

```
local lp = entities.get_local_pawn();
```

### get\_local\_controller﻿ <a href="#get-local-controller" id="get-local-controller"></a>

Function

Returns the local player's controller.

Arguments

None.

Returns

| Type                                                                           | Description |
| ------------------------------------------------------------------------------ | ----------- |
| [`cs2_player_controller`](https://lua.fatality.win/cs2-player-controller.html) | Controller. |

Example

```
local lp_ctrl = entities.get_local_controller();
```
