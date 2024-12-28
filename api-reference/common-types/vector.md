# vector

This type is a common 3D vector (x, y, z).

> ####
>
> This type supports operations, such as `+`, `-`, `/`, `*` and `==`.

### x﻿ <a href="#x" id="x"></a>

Field

Type: `float`

X coordinate.

### y﻿ <a href="#y" id="y"></a>

Field

Type: `float`

Y coordinate.

### z﻿ <a href="#z" id="z"></a>

Field

Type: `float`

Z coordinate.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs a vector.

Arguments

1\. Default vector (0, 0, 0).

None.

2\. Single value.

| Name    | Type    | Description          |
| ------- | ------- | -------------------- |
| `value` | `float` | X and Y coordinates. |

3\. XYZ values.

| Name | Type    | Description   |
| ---- | ------- | ------------- |
| `x`  | `float` | X coordinate. |
| `y`  | `float` | Y coordinate. |
| `z`  | `float` | Z coordinate. |

Returns

| Type     | Description |
| -------- | ----------- |
| `vector` | Vector.     |

Example

```
local vec = vector(5, 25, 12);
```

### is\_zero﻿ <a href="#is-zero" id="is-zero"></a>

Method

Returns `true` if this vector is within tolerance range.

Arguments

| Name        | Type    | Description                                |
| ----------- | ------- | ------------------------------------------ |
| `tolerance` | `float` | Max allowed tolerance. Defaults to `0.01`. |

Returns

| Type   | Description                                            |
| ------ | ------------------------------------------------------ |
| `bool` | `true` if ranges between `-tolerance` and `tolerance`. |

Example

```
local vec = vector(0, 0.1, 0.5);
print(tostring(vec:is_zero(1))); -- will print 'true', because every value fits in the range of -1 and 1
```

### dist﻿ <a href="#dist" id="dist"></a>

Method

Returns distance to another vector.

Arguments

| Name    | Type     | Description                           |
| ------- | -------- | ------------------------------------- |
| `other` | `vector` | Vector to calculate distance against. |

Returns

| Type    | Description               |
| ------- | ------------------------- |
| `float` | Distance to other vector. |

Example

```
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist(vec2)));
```

### dist\_sqr﻿ <a href="#dist-sqr" id="dist-sqr"></a>

Method

Returns squared distance to another vector.

> ####
>
> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

Arguments

| Name    | Type     | Description                           |
| ------- | -------- | ------------------------------------- |
| `other` | `vector` | Vector to calculate distance against. |

Returns

| Type    | Description                       |
| ------- | --------------------------------- |
| `float` | Squared distance to other vector. |

Example

```
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_sqr(vec2)));
```

### dist\_2d﻿ <a href="#dist-2d" id="dist-2d"></a>

Method

Returns 2D (only `x` and `y` values) distance to another vector.

Arguments

| Name    | Type     | Description                           |
| ------- | -------- | ------------------------------------- |
| `other` | `vector` | Vector to calculate distance against. |

Returns

| Type    | Description               |
| ------- | ------------------------- |
| `float` | Distance to other vector. |

Example

```
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d(vec2)));
```

### dist\_2d\_sqr﻿ <a href="#dist-2d-sqr" id="dist-2d-sqr"></a>

Method

Returns squared 2D (only `x` and `y` values) distance to another vector.

> ####
>
> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

Arguments

| Name    | Type     | Description                           |
| ------- | -------- | ------------------------------------- |
| `other` | `vector` | Vector to calculate distance against. |

Returns

| Type    | Description                       |
| ------- | --------------------------------- |
| `float` | Squared distance to other vector. |

Example

```
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d_sqr(vec2)));
```

### cross﻿ <a href="#cross" id="cross"></a>

Method

Returns a cross product to another vector.

Arguments

| Name    | Type     | Description                                |
| ------- | -------- | ------------------------------------------ |
| `other` | `vector` | Vector to calculate cross product against. |

Returns

| Type     | Description    |
| -------- | -------------- |
| `vector` | Cross product. |

Example

```
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
local cross = vec1:cross(vec2);
```

### is\_valid﻿ <a href="#is-valid" id="is-valid"></a>

Method

Returns `true` if all values in this vector are finite.

Arguments

None.

Returns

| Type   | Description                  |
| ------ | ---------------------------- |
| `bool` | `true` if values are finite. |

Example

```
local vec = vector(5, 1, 6);
if vec:is_valid() then
    -- ...
end
```

### length﻿ <a href="#length" id="length"></a>

Method

Returns length of this vector.

Arguments

None.

Returns

| Type    | Description            |
| ------- | ---------------------- |
| `float` | Length of this vector. |

Example

```
local vec = vector(5, 1, 6);
local length = vec:length();
```

### length\_sqr﻿ <a href="#length-sqr" id="length-sqr"></a>

Method

Returns squared length of this vector.

> ####
>
> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

Arguments

None.

Returns

| Type    | Description            |
| ------- | ---------------------- |
| `float` | Length of this vector. |

Example

```
local vec = vector(5, 1, 6);
local length = vec:length_sqr();
```

### length\_2d﻿ <a href="#length-2d" id="length-2d"></a>

Method

Returns 2D length of this vector.

Arguments

None.

Returns

| Type    | Description            |
| ------- | ---------------------- |
| `float` | Length of this vector. |

Example

```
local vec = vector(5, 1, 6);
local length = vec:length_2d();
```

### length\_2d\_sqr﻿ <a href="#length-2d-sqr" id="length-2d-sqr"></a>

Method

Returns squared 2D length of this vector.

> ####
>
> This method is de-facto faster than the non-squared variant. Use it, if you need extra performance.

Arguments

None.

Returns

| Type    | Description            |
| ------- | ---------------------- |
| `float` | Length of this vector. |

Example

```
local vec = vector(5, 1, 6);
local length = vec:length_2d_sqr();
```

### dot﻿ <a href="#dot" id="dot"></a>

Method

Returns dot product of 2 vectors.

Arguments

| Name    | Type     | Description                              |
| ------- | -------- | ---------------------------------------- |
| `other` | `vector` | Vector to calculate dot product against. |

Returns

| Type    | Description  |
| ------- | ------------ |
| `float` | Dot product. |

Example

```
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
local dot = vec1:dot(vec2);
```
