# color

This type is a color used within the rendering system.

> ####
>
> Do not mistake this type with [`color`](https://lua.fatality.win/color.html) that is used in game! While these types are interchangeable internally, they are NOT in the API.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Creates a new color instance.

Arguments

1\. Default color (translucent black).

None.

2\. Integer colors.

| Name | Type  | Description                                |
| ---- | ----- | ------------------------------------------ |
| `r`  | `int` | Red color (`0` to `255`).                  |
| `g`  | `int` | Green color (`0` to `255`).                |
| `b`  | `int` | Blue color (`0` to `255`).                 |
| `a`  | `int` | Opacity (`0` to `255`). Defaults to `255`. |

3\. Hex string.

| Name  | Type     | Description                                                          |
| ----- | -------- | -------------------------------------------------------------------- |
| `hex` | `string` | Hex string. Formats are: `#rrggbbaa`, `#rrggbb`, `#rgba` and `#rgb`. |

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local white = draw.color(255, 255, 255);
```

### white﻿ <a href="#white" id="white"></a>

Function

Returns a white, opaque color.

Arguments

None.

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local white = draw.color.white();
```

### white\_transparent﻿ <a href="#white-transparent" id="white-transparent"></a>

Function

Returns a white, transparent color.

Arguments

None.

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local white_t = draw.color.white_transparent();
```

### black﻿ <a href="#black" id="black"></a>

Function

Returns a black, opaque color.

Arguments

None.

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local black = draw.color.black();
```

### black\_transparent﻿ <a href="#black-transparent" id="black-transparent"></a>

Function

Returns a black, transparent color.

Arguments

None.

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local black_t = draw.color.black_transparent();
```

### percent﻿ <a href="#percent" id="percent"></a>

Function

Returns a red-to-green color, depending on the provided percent.

Arguments

| Name | Type    | Description               |
| ---- | ------- | ------------------------- |
| `p`  | `float` | Percentile (`0` to `1`).  |
| `a`  | `float` | Opacity. Defaults to `1`. |

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local yellow = draw.color.percent(0.5);
```

### gray﻿ <a href="#gray" id="gray"></a>

Function

Returns a black-to-white color, depending on the provided percent.

Arguments

| Name | Type    | Description               |
| ---- | ------- | ------------------------- |
| `b`  | `float` | Percentile (`0` to `1`).  |
| `a`  | `float` | Opacity. Defaults to `1`. |

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local gray = draw.color.gray(0.5);
```

### interpolate﻿ <a href="#interpolate" id="interpolate"></a>

Function

Interpolates two colors.

Arguments

| Name | Type    | Description               |
| ---- | ------- | ------------------------- |
| `a`  | `color` | Starting color.           |
| `b`  | `color` | Ending color.             |
| `t`  | `float` | Interpolation percentile. |

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Color object. |

Example

```
local a = draw.color.white();
local b = draw.color.black();
local i = draw.color.interpolate(a, b, 0.5); -- gray
```

### rgba﻿ <a href="#rgba" id="rgba"></a>

Method

Returns integer representation of this color (RGBA format)

Arguments

None.

Returns

| Type  | Description |
| ----- | ----------- |
| `int` | RGBA color. |

Example

```
local num = col:rgba();
```

### argb﻿ <a href="#argb" id="argb"></a>

Method

Returns integer representation of this color (ARGB format)

Arguments

None.

Returns

| Type  | Description |
| ----- | ----------- |
| `int` | ARGB color. |

Example

```
local num = col:argb();
```

### bgra﻿ <a href="#bgra" id="bgra"></a>

Method

Returns integer representation of this color (BGRA format)

Arguments

None.

Returns

| Type  | Description |
| ----- | ----------- |
| `int` | BGRA color. |

Example

```
local num = col:bgra();
```

### abgr﻿ <a href="#abgr" id="abgr"></a>

Method

Returns integer representation of this color (ABGR format)

Arguments

None.

Returns

| Type  | Description |
| ----- | ----------- |
| `int` | ABGR color. |

Example

```
local num = col:abgr();
```

### darken﻿ <a href="#darken" id="darken"></a>

Method

Returns darker variant of this color.

Arguments

| Name    | Type    | Description                     |
| ------- | ------- | ------------------------------- |
| `value` | `float` | Modulation amount (`0` to `1`). |

Returns

| Type    | Description   |
| ------- | ------------- |
| `color` | Darker color. |

Example

```
local darker = col:darken(0.5);
```

### mod\_a﻿ <a href="#mod-a" id="mod-a"></a>

Method

Modulate opacity of the color. This will take existing opacity, and multiply it by whatever value you provide. It is useful if you want to modulate same color in steps, instead of setting the accurate opacity number.

Arguments

1\. Float variant.

| Name    | Type    | Description                      |
| ------- | ------- | -------------------------------- |
| `value` | `float` | Opacity modulation (`0` to `1`). |

2\. Integer variant.

| Name    | Type  | Description                        |
| ------- | ----- | ---------------------------------- |
| `value` | `int` | Opacity modulation (`0` to `255`). |

Returns

| Type    | Description      |
| ------- | ---------------- |
| `color` | Modulated color. |

Example

```
local half_opacity = col:mod_a(0.5);
```

### r﻿ <a href="#r" id="r"></a>

Method

Override red and return new color.

Arguments

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| `value` | `float` | New value.  |

Returns

| Type    | Description |
| ------- | ----------- |
| `color` | New color.  |

Example

```
local full_red = col:r(1);
```

### g﻿ <a href="#g" id="g"></a>

Method

Override green and return new color.

Arguments

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| `value` | `float` | New value.  |

Returns

| Type    | Description |
| ------- | ----------- |
| `color` | New color.  |

Example

```
local full_green = col:g(1);
```

### b﻿ <a href="#b" id="b"></a>

Method

Override blue and return new color.

Arguments

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| `value` | `float` | New value.  |

Returns

| Type    | Description |
| ------- | ----------- |
| `color` | New color.  |

Example

```
local full_blue = col:b(1);
```

### a﻿ <a href="#a" id="a"></a>

Method

Override opacity and return new color.

Arguments

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| `value` | `float` | New value.  |

Returns

| Type    | Description |
| ------- | ----------- |
| `color` | New color.  |

Example

```
local full_opacity = col:a(1);
```

### get\_r﻿ <a href="#get-r" id="get-r"></a>

Method

Returns red color value.

Arguments

None.

Returns

| Type  | Description  |
| ----- | ------------ |
| `int` | Color value. |

Example

```
local r = col:get_r();
```

### get\_g﻿ <a href="#get-g" id="get-g"></a>

Method

Returns green color value.

Arguments

None.

Returns

| Type  | Description  |
| ----- | ------------ |
| `int` | Color value. |

Example

```
local g = col:get_g();
```

### get\_b﻿ <a href="#get-b" id="get-b"></a>

Method

Returns blue color value.

Arguments

None.

Returns

| Type  | Description  |
| ----- | ------------ |
| `int` | Color value. |

Example

```
local b = col:get_b();
```

### get\_a﻿ <a href="#get-a" id="get-a"></a>

Method

Returns opacity color value.

Arguments

None.

Returns

| Type  | Description  |
| ----- | ------------ |
| `int` | Color value. |

Example

```
local a = col:get_a();
```

### h﻿ <a href="#h" id="h"></a>

Method

Return hue value of the color.

Arguments

None.

Returns

| Type  | Description         |
| ----- | ------------------- |
| `int` | Hue (`0` to `359`). |

Example

```
local hue = col:h();
```

### s﻿ <a href="#s" id="s"></a>

Method

Returns saturation value of the color.

Arguments

None.

Returns

| Type    | Description              |
| ------- | ------------------------ |
| `float` | Saturation (`0` to `1`). |

Example

```
local saturation = col:s();
```

### v﻿ <a href="#v" id="v"></a>

Method

Returns brightness value of the color.

Arguments

None.

Returns

| Type    | Description              |
| ------- | ------------------------ |
| `float` | Brightness (`0` to `1`). |

Example

```
local brightness = col:v();
```

### hsv﻿ <a href="#hsv" id="hsv"></a>

Method

Construct new color from provided HSB values.

Arguments

| Name         | Type    | Description                                                                                  |
| ------------ | ------- | -------------------------------------------------------------------------------------------- |
| `hue`        | `int`   | Hue (`0` to `359`).                                                                          |
| `saturation` | `float` | Saturation (`0` to `1`).                                                                     |
| `brightness` | `float` | Brightness (`0` to `1`).                                                                     |
| `alpha`      | `float` | Override opacity of the source color. Must be either left out, or provided `0` to `1` value. |

Returns

| Type    | Description |
| ------- | ----------- |
| `color` | New color.  |

Example

```
local new_col = col:hsv(250, 0.5, 0.1);
```
