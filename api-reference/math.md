# math

Usage:

`math.{func}`

This table extends the existing `math` table that is a part of Lua.

### calc\_angle﻿ <a href="#calc-angle" id="calc-angle"></a>

Function

Calculates angles between 2 vectors.

Arguments

| Name  | Type                                             | Description         |
| ----- | ------------------------------------------------ | ------------------- |
| `src` | [`vector`](https://lua.fatality.win/vector.html) | Source vector.      |
| `dst` | [`vector`](https://lua.fatality.win/vector.html) | Destination vector. |

Returns

| Type                                             | Description |
| ------------------------------------------------ | ----------- |
| [`vector`](https://lua.fatality.win/vector.html) | Angles.     |

Example

```
local ang = math.calc_angle(vec1, vec2);
```

### angle\_normalize﻿ <a href="#angle-normalize" id="angle-normalize"></a>

Function

Normalizes an angle.

Arguments

| Name    | Type    | Description  |
| ------- | ------- | ------------ |
| `angle` | `float` | Input angle. |

Returns

| Type    | Description       |
| ------- | ----------------- |
| `float` | Normalized angle. |

Example

```
local norm = math.angle_normalize(560);
```

### approach\_angles﻿ <a href="#approach-angles" id="approach-angles"></a>

Function

Approaches an angle over time.

Arguments

| Name    | Type                                             | Description     |
| ------- | ------------------------------------------------ | --------------- |
| `from`  | [`vector`](https://lua.fatality.win/vector.html) | Start angle.    |
| `to`    | [`vector`](https://lua.fatality.win/vector.html) | End angle.      |
| `speed` | `float`                                          | Approach speed. |

Returns

| Type                                             | Description  |
| ------------------------------------------------ | ------------ |
| [`vector`](https://lua.fatality.win/vector.html) | Delta angle. |

Example

```
local ang = math.approach_angles(from, to, 1.0 / game.global_vars.frametime);
```

### edge\_point﻿ <a href="#edge-point" id="edge-point"></a>

Function

Returns a point on the edge of a box.

Arguments

| Name     | Type                                             | Description              |
| -------- | ------------------------------------------------ | ------------------------ |
| `mins`   | [`vector`](https://lua.fatality.win/vector.html) | Box mins.                |
| `maxs`   | [`vector`](https://lua.fatality.win/vector.html) | Box maxs.                |
| `dir`    | [`vector`](https://lua.fatality.win/vector.html) | Point direction (angle). |
| `radius` | `float`                                          | Area radius.             |

Returns

| Type                                             | Description |
| ------------------------------------------------ | ----------- |
| [`vector`](https://lua.fatality.win/vector.html) | Point.      |

Example

```
local point = math.edge_point(mins, maxs, dir, 5);
```

### lerp﻿ <a href="#lerp" id="lerp"></a>

Function

Linear interpolation.

Arguments

| Name       | Type    | Description           |
| ---------- | ------- | --------------------- |
| `t1`       | `float` | Start value.          |
| `t2`       | `float` | End value.            |
| `progress` | `float` | Interpolation amount. |

Returns

| Type    | Description         |
| ------- | ------------------- |
| `float` | Interpolated value. |

Example

```
local mid = math.lerp(0, 100, 0.5);
```

### vector\_angles﻿ <a href="#vector-angles" id="vector-angles"></a>

Function

Calculates angles from a vector.

Arguments

| Name      | Type                                             | Description                   |
| --------- | ------------------------------------------------ | ----------------------------- |
| `forward` | [`vector`](https://lua.fatality.win/vector.html) | Source vector.                |
| `up`      | [`vector`](https://lua.fatality.win/vector.html) | Up vector. Defaults to `nil`. |

Returns

| Type                                             | Description |
| ------------------------------------------------ | ----------- |
| [`vector`](https://lua.fatality.win/vector.html) | Angles.     |

Example

```
local ang = math.vector_angles(fw);
```

### world\_to\_screen﻿ <a href="#world-to-screen" id="world-to-screen"></a>

Function

Transforms a point in the game world onto the viewport.

Arguments

| Name    | Type                                             | Description                                          |
| ------- | ------------------------------------------------ | ---------------------------------------------------- |
| `xyz`   | [`vector`](https://lua.fatality.win/vector.html) | Point in the world.                                  |
| `round` | `bool`                                           | Whether should round the output. Defaults to `true`. |

Returns

| Type                                         | Description            |
| -------------------------------------------- | ---------------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Point on the viewport. |

Example

```
local point = math.world_to_screen(game_point);
```

### clamp﻿ <a href="#clamp" id="clamp"></a>

Function

Clamps a value between min and max.

Arguments

| Name    | Type    | Description    |
| ------- | ------- | -------------- |
| `n`     | `float` | Value.         |
| `lower` | `float` | Lowest value.  |
| `upper` | `float` | Highest value. |

Returns

| Type    | Description    |
| ------- | -------------- |
| `float` | Clamped value. |

Example

```
local x = math.clamp(50, 5, 25); -- 25
```

### remap\_val﻿ <a href="#remap-val" id="remap-val"></a>

Function

Maps the value from one range to another range.

Arguments

| Name  | Type    | Description                |
| ----- | ------- | -------------------------- |
| `val` | `float` | Value.                     |
| `a`   | `float` | Lowest source value.       |
| `b`   | `float` | Highest source value.      |
| `c`   | `float` | Lowest destination value.  |
| `d`   | `float` | Highest destination value. |

Returns

| Type    | Description   |
| ------- | ------------- |
| `float` | Mapped value. |

Example

```
local mapped = math.remap_val(0.5, 0, 1, 0, 100); -- 50
```

### remap\_val\_clamped﻿ <a href="#remap-val-clamped" id="remap-val-clamped"></a>

Function

Maps the value from one range to another range. Additionally, clamps the value based on the source range.

Arguments

| Name  | Type    | Description                |
| ----- | ------- | -------------------------- |
| `val` | `float` | Value.                     |
| `a`   | `float` | Lowest source value.       |
| `b`   | `float` | Highest source value.      |
| `c`   | `float` | Lowest destination value.  |
| `d`   | `float` | Highest destination value. |

Returns

| Type    | Description   |
| ------- | ------------- |
| `float` | Mapped value. |

Example

```
local mapped = math.remap_val_clamped(5, 0, 1, 0, 100); -- 100
```

### vec2﻿ <a href="#vec2" id="vec2"></a>

Function

An alias to [`draw.vec2()`](https://lua.fatality.win/vec2.html#call).

Example

```
local vec = math.vec2(5, 5);
```

### vec3﻿ <a href="#vec3" id="vec3"></a>

Function

An alias to [`vector()`](https://lua.fatality.win/vector.html#call).

Example

```
local vec = math.vec3(5, 12, 5);
```
