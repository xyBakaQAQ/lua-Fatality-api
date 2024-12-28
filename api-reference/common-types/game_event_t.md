# game\_event\_t

Describes a game event.

### get\_name﻿ <a href="#get-name" id="get-name"></a>

Method

Returns the event name.

Arguments

None.

Returns

| Type     | Description |
| -------- | ----------- |
| `string` | Event name. |

Example

```
if event:get_name() == 'player_hurt' then
    -- ...
end
```

### get\_bool﻿ <a href="#get-bool" id="get-bool"></a>

Method

Returns the boolean value by key.

Arguments

| Name  | Type     | Description |
| ----- | -------- | ----------- |
| `key` | `string` | Entry key.  |

Returns

| Type   | Description                                             |
| ------ | ------------------------------------------------------- |
| `bool` | Entry value. Returns `false` if such key was not found. |

Example

```
event:get_bool('some_key');
```

### get\_int﻿ <a href="#get-int" id="get-int"></a>

Method

Returns the integer value by key.

Arguments

| Name  | Type     | Description |
| ----- | -------- | ----------- |
| `key` | `string` | Entry key.  |

Returns

| Type  | Description                                         |
| ----- | --------------------------------------------------- |
| `int` | Entry value. Returns `0` if such key was not found. |

Example

```
event:get_int('some_key');
```

### get\_float﻿ <a href="#get-float" id="get-float"></a>

Method

Returns the float value by key.

Arguments

| Name  | Type     | Description |
| ----- | -------- | ----------- |
| `key` | `string` | Entry key.  |

Returns

| Type    | Description                                           |
| ------- | ----------------------------------------------------- |
| `float` | Entry value. Returns `0.0` if such key was not found. |

Example

```
event:get_float('some_key');
```

### get\_string﻿ <a href="#get-string" id="get-string"></a>

Method

Returns the string value by key.

Arguments

| Name  | Type     | Description |
| ----- | -------- | ----------- |
| `key` | `string` | Entry key.  |

Returns

| Type     | Description                                          |
| -------- | ---------------------------------------------------- |
| `string` | Entry value. Returns `''` if such key was not found. |

Example

```
event:get_string('some_key');
```

### get\_controller﻿ <a href="#get-controller" id="get-controller"></a>

Method

Returns the controller by key.

Arguments

| Name  | Type     | Description |
| ----- | -------- | ----------- |
| `key` | `string` | Entry key.  |

Returns

| Type                                                                           | Description |
| ------------------------------------------------------------------------------ | ----------- |
| [`cs2_player_controller`](https://lua.fatality.win/cs2-player-controller.html) | Controller. |

Example

```
event:get_controller('userid');
```

### get\_pawn\_from\_id﻿ <a href="#get-pawn-from-id" id="get-pawn-from-id"></a>

Method

Returns the pawn by key.

Arguments

| Name  | Type     | Description |
| ----- | -------- | ----------- |
| `key` | `string` | Entry key.  |

Returns

| Type                                                               | Description |
| ------------------------------------------------------------------ | ----------- |
| [`cs2_player_pawn`](https://lua.fatality.win/cs2-player-pawn.html) | Pawn.       |

Example

```
event:get_pawn_from_id('userid');
```
