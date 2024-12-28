# rect

This type is a rectangle used within rendering system.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Creates a new rectangle.

Arguments

1\. Default rectangle (0, 0 position; 0, 0 size).

None.

2\. Single value.

| Name    | Type    | Description             |
| ------- | ------- | ----------------------- |
| `value` | `float` | Mins XY, maxs XY value. |

3\. Single vector.

| Name    | Type                                         | Description               |
| ------- | -------------------------------------------- | ------------------------- |
| `value` | [`vec2`](https://lua.fatality.win/vec2.html) | Mins vector, maxs vector. |

4\. Double value.

| Name | Type    | Description             |
| ---- | ------- | ----------------------- |
| `x`  | `float` | Mins/maxs X coordinate. |
| `y`  | `float` | Mins/maxs Y coordinate. |

5\. Double vector.

| Name   | Type                                         | Description  |
| ------ | -------------------------------------------- | ------------ |
| `mins` | [`vec2`](https://lua.fatality.win/vec2.html) | Mins vector. |
| `maxs` | [`vec2`](https://lua.fatality.win/vec2.html) | Maxs vector. |

6\. Four values.

| Name | Type    | Description        |
| ---- | ------- | ------------------ |
| `x0` | `float` | Mins X coordinate. |
| `y0` | `float` | Mins Y coordinate. |
| `x1` | `float` | Maxs X coordinate. |
| `y1` | `float` | Maxs Y coordinate. |

Returns

| Type   | Description    |
| ------ | -------------- |
| `rect` | New rectangle. |

Example

```
local my_rect = draw.rect(50, 50, 150, 150);
```

### mins﻿ <a href="#mins" id="mins"></a>

Field

Type: [`vec2`](https://lua.fatality.win/vec2.html)

Mins (top-left) vector.

### maxs﻿ <a href="#maxs" id="maxs"></a>

Field

Type: [`vec2`](https://lua.fatality.win/vec2.html)

Maxs (bottom-right) vector.

### width﻿ <a href="#width" id="width"></a>

Method

Either returns rectangle's width, or sets a new width.

Arguments

1\. Get width.

None.

2\. Set width.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| `value` | `float` | New width.  |

Returns

1\. Get width.

| Type    | Description |
| ------- | ----------- |
| `float` | Width.      |

2\. Set width.

| Type   | Description                       |
| ------ | --------------------------------- |
| `rect` | New rectangle with changed width. |

Example

```
local half_width = rect:width(rect:width() * 0.5);
```

### height﻿ <a href="#height" id="height"></a>

Method

Either returns rectangle's height, or sets a new height.

Arguments

1\. Get height.

None.

2\. Set height.

| Name    | Type    | Description |
| ------- | ------- | ----------- |
| `value` | `float` | New height. |

Returns

1\. Get height.

| Type    | Description |
| ------- | ----------- |
| `float` | Height.     |

2\. Set height.

| Type   | Description                        |
| ------ | ---------------------------------- |
| `rect` | New rectangle with changed height. |

Example

```
local half_height = rect:height(rect:height() * 0.5);
```

### size﻿ <a href="#size" id="size"></a>

Method

Either returns rectangle's size, or sets a new size.

Arguments

1\. Get size.

None.

2\. Set size.

| Name    | Type                                         | Description |
| ------- | -------------------------------------------- | ----------- |
| `value` | [`vec2`](https://lua.fatality.win/vec2.html) | New size.   |

Returns

1\. Get size.

| Type                                         | Description |
| -------------------------------------------- | ----------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Size.       |

2\. Set size.

| Type   | Description                      |
| ------ | -------------------------------- |
| `rect` | New rectangle with changed size. |

Example

```
local half_size = rect:size(rect:size() * draw.vec2(0.5, 0.5));
```

### explode﻿ <a href="#explode" id="explode"></a>

Method

Explodes the rectangle by given vector (increase size from center into all directions by coordinates in the vector).

Arguments

| Name    | Type                                         | Description   |
| ------- | -------------------------------------------- | ------------- |
| `value` | [`vec2`](https://lua.fatality.win/vec2.html) | Explode size. |

Returns

| Type   | Description         |
| ------ | ------------------- |
| `rect` | Exploded rectangle. |

Example

```
local exp = rect:explode(draw.vec2(6, 6)); -- will subtract -3,-3 from mins and add 3,3 to maxs
```

### half\_width﻿ <a href="#half-width" id="half-width"></a>

Method

Returns a rectangle with half of the width of this rectangle.

Arguments

None.

Returns

| Type   | Description                  |
| ------ | ---------------------------- |
| `rect` | Rectangle with halved width. |

Example

```
local half = rect:half_width();
```

### translate﻿ <a href="#translate" id="translate"></a>

Method

Translates (moves) this rectangle by vector coordinates.

Arguments

| Name    | Type                                         | Description         |
| ------- | -------------------------------------------- | ------------------- |
| `value` | [`vec2`](https://lua.fatality.win/vec2.html) | Translation amount. |

Returns

| Type   | Description           |
| ------ | --------------------- |
| `rect` | Translated rectangle. |

Example

```
local rect = draw.rect(50, 50, 150, 150);
local translated = rect:translate(draw.vec2(5, 5)); -- mins/maxs will be 55,55 and 155,155
```

### margin\_left﻿ <a href="#margin-left" id="margin-left"></a>

Method

Move rectangle from the left by given amount.

Arguments

| Name    | Type    | Description    |
| ------- | ------- | -------------- |
| `value` | `float` | Margin amount. |

Returns

| Type   | Description      |
| ------ | ---------------- |
| `rect` | Moved rectangle. |

Example

```
local new = rect:margin_left(5); -- moves to the right by 5px
```

### margin\_right﻿ <a href="#margin-right" id="margin-right"></a>

Method

Move rectangle from the right by given amount.

Arguments

| Name    | Type    | Description    |
| ------- | ------- | -------------- |
| `value` | `float` | Margin amount. |

Returns

| Type   | Description      |
| ------ | ---------------- |
| `rect` | Moved rectangle. |

Example

```
local new = rect:margin_right(5); -- moves to the left by 5px
```

### margin\_top﻿ <a href="#margin-top" id="margin-top"></a>

Method

Move rectangle from the top by given amount.

Arguments

| Name    | Type    | Description    |
| ------- | ------- | -------------- |
| `value` | `float` | Margin amount. |

Returns

| Type   | Description      |
| ------ | ---------------- |
| `rect` | Moved rectangle. |

Example

```
local new = rect:margin_top(5); -- moves to the bottom by 5px
```

### margin\_bottom﻿ <a href="#margin-bottom" id="margin-bottom"></a>

Method

Move rectangle from the bottom by given amount.

Arguments

| Name    | Type    | Description    |
| ------- | ------- | -------------- |
| `value` | `float` | Margin amount. |

Returns

| Type   | Description      |
| ------ | ---------------- |
| `rect` | Moved rectangle. |

Example

```
local new = rect:margin_bottom(5); -- moves to the top by 5px
```

### padding\_left﻿ <a href="#padding-left" id="padding-left"></a>

Method

Adds the value to the left side of the rectangle.

Arguments

| Name    | Type    | Description     |
| ------- | ------- | --------------- |
| `value` | `float` | Padding amount. |

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Resized rectangle. |

Example

```
local new = rect:padding_left(5); -- adds 5 to mins x
```

### padding\_right﻿ <a href="#padding-right" id="padding-right"></a>

Method

Adds the value to the right side of the rectangle.

Arguments

| Name    | Type    | Description     |
| ------- | ------- | --------------- |
| `value` | `float` | Padding amount. |

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Resized rectangle. |

Example

```
local new = rect:padding_right(5); -- adds 5 to maxs x
```

### padding\_top﻿ <a href="#padding-top" id="padding-top"></a>

Method

Adds the value to the top side of the rectangle.

Arguments

| Name    | Type    | Description     |
| ------- | ------- | --------------- |
| `value` | `float` | Padding amount. |

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Resized rectangle. |

Example

```
local new = rect:padding_top(5); -- adds 5 to mins y
```

### padding\_bottom﻿ <a href="#padding-bottom" id="padding-bottom"></a>

Method

Adds the value to the bottom side of the rectangle.

Arguments

| Name    | Type    | Description     |
| ------- | ------- | --------------- |
| `value` | `float` | Padding amount. |

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Resized rectangle. |

Example

```
local new = rect:padding_bottom(5); -- adds 5 to maxs y
```

### shrink﻿ <a href="#shrink" id="shrink"></a>

Method

Shrinks (implodes) the rectangle by given amount.

Arguments

| Name    | Type    | Description   |
| ------- | ------- | ------------- |
| `value` | `float` | Shrink value. |

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Resized rectangle. |

Example

```
local shrinked = rect:shrink(5); -- adds 5,5 to mins and subtracts 5,5 from maxs
```

### expand﻿ <a href="#expand" id="expand"></a>

Method

Expands (explodes) the rectangle by given amount.

Arguments

| Name    | Type    | Description   |
| ------- | ------- | ------------- |
| `value` | `float` | Expand value. |

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Resized rectangle. |

Example

```
local expanded = rect:expand(5); -- subtracts 5,5 from mins and adds 5,5 to maxs
```

### contains﻿ <a href="#contains" id="contains"></a>

Method

Returns `true` if this rectangle contains either vector or another rectangle.

> ####
>
> Rectangle overload will return `true` ONLY of entire other rectangle is within the bounds of this one.

Arguments

1\. Vector variant.

| Name    | Type                                         | Description              |
| ------- | -------------------------------------------- | ------------------------ |
| `other` | [`vec2`](https://lua.fatality.win/vec2.html) | Vector to check against. |

2\. Rectangle variant.

| Name    | Type   | Description                 |
| ------- | ------ | --------------------------- |
| `other` | `rect` | Rectangle to check against. |

Returns

| Type   | Description                                            |
| ------ | ------------------------------------------------------ |
| `bool` | `true` if other object is in bounds of this rectangle. |

Example

```
if rect:contains(cursor_pos) then
    -- ...
end
```

### overlaps﻿ <a href="#overlaps" id="overlaps"></a>

Method

Returns `true` if the other rectangle overlaps with this rectangle.

Arguments

| Name    | Type   | Description                 |
| ------- | ------ | --------------------------- |
| `other` | `rect` | Rectangle to check against. |

Returns

| Type   | Description                                             |
| ------ | ------------------------------------------------------- |
| `bool` | `true` if other rectangle overlaps with this rectangle. |

Example

```
if rect:overlaps(another_rect) then
    -- ...
end
```

### intersect﻿ <a href="#intersect" id="intersect"></a>

Method

Intersects this rectangle with another rectangle.

Arguments

| Name    | Type   | Description                  |
| ------- | ------ | ---------------------------- |
| `other` | `rect` | Rectangle to intersect with. |

Returns

| Type   | Description            |
| ------ | ---------------------- |
| `rect` | Intersected rectangle. |

Example

```
local intersected = rect:intersect(another_rect);
```

### tl﻿ <a href="#tl" id="tl"></a>

Method

Returns top-left vector.

Arguments

None.

Returns

| Type                                         | Description      |
| -------------------------------------------- | ---------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Top-left vector. |

Example

```
local tl = rect:tl();
```

### tr﻿ <a href="#tr" id="tr"></a>

Method

Returns top-right vector.

Arguments

None.

Returns

| Type                                         | Description       |
| -------------------------------------------- | ----------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Top-right vector. |

Example

```
local tr = rect:tr();
```

### br﻿ <a href="#br" id="br"></a>

Method

Returns bottom-right vector.

Arguments

None.

Returns

| Type                                         | Description          |
| -------------------------------------------- | -------------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Bottom-right vector. |

Example

```
local br = rect:br();
```

### bl﻿ <a href="#bl" id="bl"></a>

Method

Returns bottom-left vector.

Arguments

None.

Returns

| Type                                         | Description         |
| -------------------------------------------- | ------------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Bottom-left vector. |

Example

```
local bl = rect:bl();
```

### center﻿ <a href="#center" id="center"></a>

Method

Returns center point of this rectangle.

Arguments

None.

Returns

| Type                                         | Description   |
| -------------------------------------------- | ------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Center point. |

Example

```
local center = rect:center();
```

### circle﻿ <a href="#circle" id="circle"></a>

Method

Treats this rectangle as an ellipsis and returns point on it. Note, that this "ellipsis" will be perfect with no modified curvature (basically if this rectangle is a box - you will get a point on a perfect circle).

Arguments

| Name | Type    | Description    |
| ---- | ------- | -------------- |
| `r`  | `float` | Radians value. |

Returns

| Type                                         | Description            |
| -------------------------------------------- | ---------------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Point on the ellipsis. |

Example

```
local point = rect:circle(rad(250)); -- returns point on the 250th degree
```

### floor﻿ <a href="#floor" id="floor"></a>

Method

Returns floored rectangle.

Arguments

None.

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Floored rectangle. |

Example

```
local floored = rect:floor();
```

### ceil﻿ <a href="#ceil" id="ceil"></a>

Method

Returns ceiled rectangle.

Arguments

None.

Returns

| Type   | Description       |
| ------ | ----------------- |
| `rect` | Ceiled rectangle. |

Example

```
local ceiled = rect:ceil();
```

### round﻿ <a href="#round" id="round"></a>

Method

Returns rounded rectangle.

Arguments

None.

Returns

| Type   | Description        |
| ------ | ------------------ |
| `rect` | Rounded rectangle. |

Example

```
local rounded = rect:round();
```

### is\_zero﻿ <a href="#is-zero" id="is-zero"></a>

Method

Returns `true` if both mins and maxs are equal to 0.

Arguments

None.

Returns

| Type   | Description                         |
| ------ | ----------------------------------- |
| `bool` | `true` if this is a zero rectangle. |

Example

```
if rect:is_zero() then
    -- ...
end
```
