# vec2

This type is a 2D vector used within the rendering system.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Creates a new 2D vector instance.

Arguments

1\. Default vector (0, 0).

None.

2\. Single value.

| Name    | Type    | Description          |
| ------- | ------- | -------------------- |
| `value` | `float` | X and Y coordinates. |

3\. XY values.

| Name | Type    | Description   |
| ---- | ------- | ------------- |
| `x`  | `float` | X coordinate. |
| `y`  | `float` | Y coordinate. |

Returns

| Type   | Description |
| ------ | ----------- |
| `vec2` | New vector. |

Example

```
local vec = draw.vec2(5, 10);
```

### x﻿ <a href="#x" id="x"></a>

Field

Type: `float`

X coordinate.

### y﻿ <a href="#y" id="y"></a>

Field

Type: `float`

Y coordinate.

### floor﻿ <a href="#floor" id="floor"></a>

Method

Returns floored variant of this vector.

Arguments

None.

Returns

| Type   | Description      |
| ------ | ---------------- |
| `vec2` | Floored variant. |

Example

```
local fl = vec:floor();
```

### ceil﻿ <a href="#ceil" id="ceil"></a>

Method

Returns ceiled variant of this vector.

Arguments

None.

Returns

| Type   | Description     |
| ------ | --------------- |
| `vec2` | Ceiled variant. |

Example

```
local ceiled = vec:ceil();
```

### round﻿ <a href="#round" id="round"></a>

Method

Returns rounded variant of this vector.

Arguments

None.

Returns

| Type   | Description      |
| ------ | ---------------- |
| `vec2` | Rounded variant. |

Example

```
local rounded = vec:round();
```

### len﻿ <a href="#len" id="len"></a>

Method

Returns length of this vector.

Arguments

None.

Returns

| Type    | Description |
| ------- | ----------- |
| `float` | Length.     |

Example

```
local len = vec:len();
```

### len\_sqr﻿ <a href="#len-sqr" id="len-sqr"></a>

Method

Returns squared length of this vector.

> ####
>
> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

Arguments

None.

Returns

| Type    | Description |
| ------- | ----------- |
| `float` | Length.     |

Example

```
local len = vec:len_sqr();
```

### dist﻿ <a href="#dist" id="dist"></a>

Method

Returns distance to another vector.

Arguments

| Name    | Type   | Description   |
| ------- | ------ | ------------- |
| `other` | `vec2` | Other vector. |

Returns

| Type    | Description |
| ------- | ----------- |
| `float` | Distance.   |

Example

```
local dist = vec1:dist(vec2);
```

### dist\_sqr﻿ <a href="#dist-sqr" id="dist-sqr"></a>

Method

Returns squared distance to another vector.

> ####
>
> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

Arguments

| Name    | Type   | Description   |
| ------- | ------ | ------------- |
| `other` | `vec2` | Other vector. |

Returns

| Type    | Description |
| ------- | ----------- |
| `float` | Distance.   |

Example

```
local dist = vec1:dist_sqr(vec2);
```
