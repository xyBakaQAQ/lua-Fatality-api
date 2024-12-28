# layer

A layer is a type that is used to store render commands, as well as vertex and index data. This is the only way to push shapes and control rendering state.

### g﻿ <a href="#g" id="g"></a>

FieldRead Only

Type: [`command`](https://lua.fatality.win/command.html)

The next render command to be pushed to the queue. This is the object you want to change to, for example, set a texture, or change rendering modes.

### font﻿ <a href="#font" id="font"></a>

Field

Type: [`font_base`](https://lua.fatality.win/font-base.html)

Font to use with `add_text`. If nothing has been set, no text will get rendered.

### tex\_sz﻿ <a href="#tex-sz" id="tex-sz"></a>

Field

Type: [`vec2?`](https://lua.fatality.win/vec2.html)

Texture dimensions. This value is only required if you are trying to render rounded shapes with a texture, so the rendering system will correctly map your UV coordinates to whatever shape you are rendering.

### skip\_dpi﻿ <a href="#skip-dpi" id="skip-dpi"></a>

Field

Type: `bool`

If set to `true`, will skip global DPI scale. Defaults to `true`.

### add\_triangle\_filled﻿ <a href="#add-triangle-filled" id="add-triangle-filled"></a>

Method

Adds a filled triangle with a single color.

Arguments

| Name  | Type                                            | Description  |
| ----- | ----------------------------------------------- | ------------ |
| `a`   | [`vec2`](https://lua.fatality.win/vec2.html)    | A point.     |
| `b`   | [`vec2`](https://lua.fatality.win/vec2.html)    | B point.     |
| `c`   | [`vec2`](https://lua.fatality.win/vec2.html)    | C point.     |
| `col` | [`color`](https://lua.fatality.win/rcolor.html) | Shape color. |

Returns

Nothing.

Example

```
layer:add_triangle_filled(
    draw.vec2(50, 50), draw.vec2(25, 75),
    draw.vec2(75, 75), draw.color(255, 255, 255));
```

### add\_quad\_filled﻿ <a href="#add-quad-filled" id="add-quad-filled"></a>

Method

Adds a filled quad with a single color.

Arguments

| Name  | Type                                            | Description         |
| ----- | ----------------------------------------------- | ------------------- |
| `tl`  | [`vec2`](https://lua.fatality.win/vec2.html)    | Top left point.     |
| `tr`  | [`vec2`](https://lua.fatality.win/vec2.html)    | Top right point.    |
| `br`  | [`vec2`](https://lua.fatality.win/vec2.html)    | Bottom right point. |
| `bl`  | [`vec2`](https://lua.fatality.win/vec2.html)    | Bottom left point.  |
| `col` | [`color`](https://lua.fatality.win/rcolor.html) | Shape color.        |

Returns

Nothing.

Example

```
layer:add_quad_filled(
    draw.vec2(50, 50), draw.vec2(100, 60),
    draw.vec2(100, 100), draw.vec2(30, 70),
    draw.color(255, 255, 255));
```

### add\_rect\_filled﻿ <a href="#add-rect-filled" id="add-rect-filled"></a>

Method

Adds a filled rectangle with a single color.

Arguments

| Name  | Type                                            | Description  |
| ----- | ----------------------------------------------- | ------------ |
| `r`   | [`rect`](https://lua.fatality.win/rect.html)    | Rectangle.   |
| `col` | [`color`](https://lua.fatality.win/rcolor.html) | Shape color. |

Returns

Nothing.

Example

```
layer:add_rect_filled(draw.rect(50, 50, 150, 150), draw.color(255, 255, 255));
```

### add\_circle\_filled﻿ <a href="#add-circle-filled" id="add-circle-filled"></a>

Method

Adds a filled circle with a single color.

Arguments

| Name       | Type                                            | Description                                                                                |
| ---------- | ----------------------------------------------- | ------------------------------------------------------------------------------------------ |
| `center`   | [`vec2`](https://lua.fatality.win/vec2.html)    | Center point.                                                                              |
| `radius`   | `float`                                         | Circle radius.                                                                             |
| `c`        | [`color`](https://lua.fatality.win/rcolor.html) | Shape color.                                                                               |
| `segments` | `int`                                           | Circle segments. If set to `0`, will attempt automatic segment deduction. Defaults to `0`. |
| `fill`     | `float`                                         | Fill amount (clockwise, `0` to `1`). Defaults to `1`.                                      |

Returns

Nothing.

Example

```
layer:add_circle_filled(draw.vec2(50, 50), 10, draw.color(255, 255, 255));
```

### add\_triangle\_filled\_multicolor﻿ <a href="#add-triangle-filled-multicolor" id="add-triangle-filled-multicolor"></a>

Method

Adds a filled, multicolor triangle.

Arguments

| Name   | Type                                         | Description                                                                    |
| ------ | -------------------------------------------- | ------------------------------------------------------------------------------ |
| `a`    | [`vec2`](https://lua.fatality.win/vec2.html) | A point.                                                                       |
| `b`    | [`vec2`](https://lua.fatality.win/vec2.html) | B point.                                                                       |
| `c`    | [`vec2`](https://lua.fatality.win/vec2.html) | C point.                                                                       |
| `cols` | `table[color, color, color]`                 | Colors for each point. Colors go in the very same order as the parameter list. |

Returns

Nothing.

Example

```
layer:add_triangle_filled_multicolor(
     draw.vec2(50, 50), draw.vec2(25, 75),
     draw.vec2(75, 75), {
        draw.color(255, 0, 0),
        draw.color(0, 255, 0),
        draw.color(0, 0, 255)
     });
```

### add\_rect\_filled\_multicolor﻿ <a href="#add-rect-filled-multicolor" id="add-rect-filled-multicolor"></a>

Method

Adds a filled, multicolor rectangle.

Arguments

| Name   | Type                                         | Description                                                                         |
| ------ | -------------------------------------------- | ----------------------------------------------------------------------------------- |
| `r`    | [`rect`](https://lua.fatality.win/rect.html) | Rectangle.                                                                          |
| `cols` | `table[color, color, color, color]`          | Colors for each corner of the rectangle, in clockwise order starting from top-left. |

Returns

Nothing.

Example

```
layer:add_rect_filled_multicolor(
    draw.rect(50, 50, 150, 150), {
        draw.color(255, 0, 0),
        draw.color(0, 255, 0),
        draw.color(0, 0, 255),
        draw.color(255, 255, 0)
    });
```

### add\_circle\_filled\_multicolor﻿ <a href="#add-circle-filled-multicolor" id="add-circle-filled-multicolor"></a>

Method

Adds a filled, multicolor circle.

Arguments

| Name       | Type                                         | Description                                                                       |
| ---------- | -------------------------------------------- | --------------------------------------------------------------------------------- |
| `center`   | [`vec2`](https://lua.fatality.win/vec2.html) | Center point.                                                                     |
| `radius`   | `float`                                      | Circle radius.                                                                    |
| `cols`     | `table[color, color]`                        | Colors for the gradient, starting with the inner and ending with the outer color. |
| `segments` | `int`                                        | The number of segments to approximate the circle. Defaults to `36`.               |
| `fill`     | `float`                                      | The portion of the circle to fill, where 1.0 is a full circle. Defaults to `1.0`. |

Returns

Nothing.

Example

```
layer:add_circle_filled_multicolor(
    draw.vec2(100, 100), 50, {
        draw.color(255, 0, 0),
        draw.color(0, 0, 255)
    }, 36, 1.0);
```

### add\_quad\_filled\_multicolor﻿ <a href="#add-quad-filled-multicolor" id="add-quad-filled-multicolor"></a>

Method

Adds a filled, multicolor quad.

Arguments

| Name   | Type                                         | Description                                          |
| ------ | -------------------------------------------- | ---------------------------------------------------- |
| `tl`   | [`vec2`](https://lua.fatality.win/vec2.html) | Top left point.                                      |
| `tr`   | [`vec2`](https://lua.fatality.win/vec2.html) | Top right point.                                     |
| `br`   | [`vec2`](https://lua.fatality.win/vec2.html) | Bottom right point.                                  |
| `bl`   | [`vec2`](https://lua.fatality.win/vec2.html) | Bottom left point.                                   |
| `cols` | `table[color, color]`                        | Colors for the gradient, applied from bottom to top. |

Returns

Nothing.

Example

```
layer:add_quad_filled_multicolor(
    draw.vec2(50, 50), draw.vec2(150, 50),
    draw.vec2(150, 150), draw.vec2(50, 150), {
        draw.color(255, 0, 0),
        draw.color(0, 0, 255)
    });
```

### add\_pill\_multicolor﻿ <a href="#add-pill-multicolor" id="add-pill-multicolor"></a>

Method

Adds a multicolor pill shape.

Arguments

| Name         | Type                                         | Description                                                               |
| ------------ | -------------------------------------------- | ------------------------------------------------------------------------- |
| `mins`       | [`vec2`](https://lua.fatality.win/vec2.html) | Top left point of the pill.                                               |
| `maxs`       | [`vec2`](https://lua.fatality.win/vec2.html) | Bottom right point of the pill.                                           |
| `radius_min` | `float`                                      | The minimum radius of the pill's rounded edges.                           |
| `radius_max` | `float`                                      | The maximum radius of the pill's rounded edges.                           |
| `cols`       | `table[color, color]`                        | Colors for the gradient, applied from bottom to top.                      |
| `segments`   | `int`                                        | The number of segments for approximating rounded edges. Defaults to `16`. |

Returns

Nothing.

Example

```
layer:add_pill_multicolor(
    draw.vec2(50, 50), draw.vec2(150, 100),
    10, 20, {
        draw.color(255, 0, 0),
        draw.color(0, 0, 255)
    }, 16);
```

### add\_shadow\_line﻿ <a href="#add-shadow-line" id="add-shadow-line"></a>

Method

Adds a shadow line.

Arguments

| Name  | Type                                                     | Description                       |
| ----- | -------------------------------------------------------- | --------------------------------- |
| `r`   | [`rect`](https://lua.fatality.win/rect.html)             | Bounding box for the shadow line. |
| `dir` | [`shadow_dir`](https://lua.fatality.win/shadow-dir.html) | Shadow direction.                 |
| `a`   | `float`                                                  | Max opacity. Defaults to `0.25`.  |

Returns

Nothing.

Example

```
layer:add_shadow_line(
    draw.rect(50, 50, 150, 150), draw.shadow_dir.down, 0.25);
```

### add\_shadow\_rect﻿ <a href="#add-shadow-rect" id="add-shadow-rect"></a>

Method

Adds a shadowed rectangle.

Arguments

| Name     | Type                                         | Description                                                         |
| -------- | -------------------------------------------- | ------------------------------------------------------------------- |
| `r`      | [`rect`](https://lua.fatality.win/rect.html) | Rectangle.                                                          |
| `radius` | `float`                                      | Shadow distance, in pixels, outwards.                               |
| `bg`     | `bool`                                       | Whether to draw a background for the rectangle. Defaults to `true`. |
| `a`      | `float`                                      | Max opacity of the shadow. Defaults to `0.25`.                      |

Returns

Nothing.

Example

```
layer:add_shadow_rect(
    draw.rect(50, 50, 150, 150), 15, true, 0.25);
```

### add\_glow﻿ <a href="#add-glow" id="add-glow"></a>

Method

Adds a glow box.

Arguments

| Name     | Type                                                     | Description                                     |
| -------- | -------------------------------------------------------- | ----------------------------------------------- |
| `r`      | [`rect`](https://lua.fatality.win/rect.html)             | Box rectangle.                                  |
| `radius` | `float`                                                  | Glow distance, in pixels, outwards.             |
| `c`      | [`color`](https://lua.fatality.win/rcolor.html)          | Glow color.                                     |
| `parts`  | [`glow_parts`](https://lua.fatality.win/glow-parts.html) | Parts of the glow to enable. Defaults to `all`. |

Returns

Nothing.

Example

```
layer:add_glow(draw.rect(50, 50, 150, 150), 15, draw.color(255, 0, 0));
```

### add\_rect\_filled\_rounded﻿ <a href="#add-rect-filled-rounded" id="add-rect-filled-rounded"></a>

Method

Adds a filled, rounded rectangle.

Arguments

| Name     | Type                                                 | Description                       |
| -------- | ---------------------------------------------------- | --------------------------------- |
| `r`      | [`rect`](https://lua.fatality.win/rect.html)         | Rectangle.                        |
| `c`      | [`color`](https://lua.fatality.win/rcolor.html)      | Fill color.                       |
| `amount` | `float`                                              | Rounding amount.                  |
| `rnd`    | [`rounding`](https://lua.fatality.win/rounding.html) | Rounding mode. Defaults to `all`. |

Returns

Nothing.

Example

```
layer:add_rect_filled_rounded(
    draw.rect(50, 50, 150, 150),
    draw.color(255, 0, 0),
    10,
    draw.rounding.all
);
```

### add\_rect\_filled\_rounded\_multicolor﻿ <a href="#add-rect-filled-rounded-multicolor" id="add-rect-filled-rounded-multicolor"></a>

Method

Adds a filled, multicolor rounded rectangle.

Arguments

| Name     | Type                                                 | Description                                          |
| -------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `r`      | [`rect`](https://lua.fatality.win/rect.html)         | Rectangle.                                           |
| `c`      | `table[color, color, color, color]`                  | Fill colors. Used clockwise, starting from top left. |
| `amount` | `float`                                              | Rounding amount.                                     |
| `rnd`    | [`rounding`](https://lua.fatality.win/rounding.html) | Rounding mode. Defaults to `all`.                    |

Returns

Nothing.

Example

```
layer:add_rect_filled_rounded_multicolor(
    draw.rect(50, 50, 150, 150), {
        draw.color(255, 0, 0),
        draw.color(0, 255, 0),
        draw.color(0, 0, 255),
        draw.color(255, 255, 0)
    },
    10,
    draw.rounding.all
);
```

### add\_triangle﻿ <a href="#add-triangle" id="add-triangle"></a>

Method

Adds a stroked triangle.

Arguments

| Name        | Type                                                         | Description                        |
| ----------- | ------------------------------------------------------------ | ---------------------------------- |
| `a`         | [`vec2`](https://lua.fatality.win/vec2.html)                 | Point A.                           |
| `b`         | [`vec2`](https://lua.fatality.win/vec2.html)                 | Point B.                           |
| `c`         | [`vec2`](https://lua.fatality.win/vec2.html)                 | Point C.                           |
| `col`       | [`color`](https://lua.fatality.win/rcolor.html)              | Line color.                        |
| `thickness` | `float`                                                      | Line thickness. Defaults to `1.0`. |
| `mode`      | [`outline_mode`](https://lua.fatality.win/outline-mode.html) | Outline mode. Defaults to `inset`. |

Returns

Nothing.

Example

```
layer:add_triangle(
    draw.vec2(50, 50),
    draw.vec2(25, 75),
    draw.vec2(75, 75),
    draw.color(255, 0, 0),
    1.0,
    draw.outline_mode.inset
);
```

### add\_quad﻿ <a href="#add-quad" id="add-quad"></a>

Method

Adds a stroked quad.

Arguments

| Name        | Type                                                         | Description                        |
| ----------- | ------------------------------------------------------------ | ---------------------------------- |
| `tl`        | [`vec2`](https://lua.fatality.win/vec2.html)                 | Top-left point.                    |
| `tr`        | [`vec2`](https://lua.fatality.win/vec2.html)                 | Top-right point.                   |
| `br`        | [`vec2`](https://lua.fatality.win/vec2.html)                 | Bottom-right point.                |
| `bl`        | [`vec2`](https://lua.fatality.win/vec2.html)                 | Bottom-left point.                 |
| `c`         | [`color`](https://lua.fatality.win/rcolor.html)              | Line color.                        |
| `thickness` | `float`                                                      | Line thickness. Defaults to `1.0`. |
| `mode`      | [`outline_mode`](https://lua.fatality.win/outline-mode.html) | Outline mode. Defaults to `inset`. |

Returns

Nothing.

Example

```
layer:add_quad(
    draw.vec2(50, 50),
    draw.vec2(150, 50),
    draw.vec2(150, 150),
    draw.vec2(50, 150),
    draw.color(255, 0, 0),
    1.0,
    draw.outline_mode.inset
);
```

### add\_rect﻿ <a href="#add-rect" id="add-rect"></a>

Method

Adds a stroked rectangle.

Arguments

| Name        | Type                                                         | Description                        |
| ----------- | ------------------------------------------------------------ | ---------------------------------- |
| `r`         | [`rect`](https://lua.fatality.win/rect.html)                 | Rectangle.                         |
| `c`         | [`color`](https://lua.fatality.win/rcolor.html)              | Line color.                        |
| `thickness` | `float`                                                      | Line thickness. Defaults to `1.0`. |
| `mode`      | [`outline_mode`](https://lua.fatality.win/outline-mode.html) | Outline mode. Defaults to `inset`. |

Returns

Nothing.

Example

```
layer:add_rect(
    draw.rect(50, 50, 150, 150),
    draw.color(255, 0, 0),
    1.0,
    draw.outline_mode.inset
);
```

### add\_circle﻿ <a href="#add-circle" id="add-circle"></a>

Method

Adds a stroked circle.

Arguments

| Name        | Type                                                         | Description                        |
| ----------- | ------------------------------------------------------------ | ---------------------------------- |
| `center`    | [`vec2`](https://lua.fatality.win/vec2.html)                 | Center point.                      |
| `radius`    | `float`                                                      | Circle radius.                     |
| `c`         | [`color`](https://lua.fatality.win/rcolor.html)              | Line color.                        |
| `segments`  | `int`                                                        | Circle segments. Defaults to `36`. |
| `fill`      | `float`                                                      | Fill amount. Defaults to `1.0`.    |
| `thickness` | `float`                                                      | Line thickness. Defaults to `1.0`. |
| `mode`      | [`outline_mode`](https://lua.fatality.win/outline-mode.html) | Outline mode. Defaults to `inset`. |

Returns

Nothing.

Example

```
layer:add_circle(
    draw.vec2(100, 100),
    50,
    draw.color(255, 0, 0),
    36,
    1.0,
    1.0,
    draw.outline_mode.inset
);
```

### add\_line﻿ <a href="#add-line" id="add-line"></a>

Method

Adds a line.

Arguments

| Name        | Type                                            | Description                       |
| ----------- | ----------------------------------------------- | --------------------------------- |
| `a`         | [`vec2`](https://lua.fatality.win/vec2.html)    | Start point.                      |
| `b`         | [`vec2`](https://lua.fatality.win/vec2.html)    | End point.                        |
| `c`         | [`color`](https://lua.fatality.win/rcolor.html) | Line color.                       |
| `thickness` | `float`                                         | Line thickness. Defaults to `1.0` |

Returns

Nothing.

Example

```
layer:add_line(
    draw.vec2(50, 50),
    draw.vec2(150, 150),
    draw.color(255, 0, 0)
);
```

### add\_line\_multicolor﻿ <a href="#add-line-multicolor" id="add-line-multicolor"></a>

Method

Adds a multicolor line.

Arguments

| Name        | Type                                            | Description                        |
| ----------- | ----------------------------------------------- | ---------------------------------- |
| `a`         | [`vec2`](https://lua.fatality.win/vec2.html)    | Start point.                       |
| `b`         | [`vec2`](https://lua.fatality.win/vec2.html)    | End point.                         |
| `c`         | [`color`](https://lua.fatality.win/rcolor.html) | Start color.                       |
| `c2`        | [`color`](https://lua.fatality.win/rcolor.html) | End color.                         |
| `thickness` | `float`                                         | Line thickness. Defaults to `1.0`. |

Returns

Nothing.

Example

```
layer:add_line_multicolor(
    draw.vec2(50, 50),
    draw.vec2(150, 150),
    draw.color(255, 0, 0),
    draw.color(0, 0, 255),
    2.0
);
```

### add\_rect\_rounded﻿ <a href="#add-rect-rounded" id="add-rect-rounded"></a>

Method

Adds a rounded, filled rectangle.

Arguments

| Name        | Type                                                         | Description                        |
| ----------- | ------------------------------------------------------------ | ---------------------------------- |
| `r`         | [`rect`](https://lua.fatality.win/rect.html)                 | Rectangle.                         |
| `c`         | [`color`](https://lua.fatality.win/rcolor.html)              | Line color.                        |
| `amount`    | `float`                                                      | Rounding amount.                   |
| `rnd`       | [`rounding`](https://lua.fatality.win/rounding.html)         | Rounding mode. Defaults to `all`.  |
| `thickness` | `float`                                                      | Line thickness. Defaults to `1.0`. |
| `mode`      | [`outline_mode`](https://lua.fatality.win/outline-mode.html) | Outline mode. Defaults to `inset`. |

Returns

Nothing.

Example

```
layer:add_rect_rounded(draw.rect(50, 50, 150, 150),
    draw.color(255, 255, 255), 14);
```

### add\_text﻿ <a href="#add-text" id="add-text"></a>

Method

Adds text.

> ####
>
> If font wasn't set, this function will do nothing.

Arguments

| Name     | Type                                                        | Description                                  |
| -------- | ----------------------------------------------------------- | -------------------------------------------- |
| `p`      | [`vec2`](https://lua.fatality.win/vec2.html)                | Text origin point.                           |
| `text`   | `string`                                                    | Text.                                        |
| `c`      | [`color`](https://lua.fatality.win/rcolor.html)             | Text color.                                  |
| `params` | [`text_params?`](https://lua.fatality.win/text-params.html) | Text aligning parameters. Defaults to `nil`. |

Returns

Nothing.

Example

```
layer:add_text(draw.vec2(50, 50), 'Hello world!', draw.color(255, 255, 255));
```

### override\_clip\_rect﻿ <a href="#override-clip-rect" id="override-clip-rect"></a>

Method

Overrides clip rectangle with support of intersection.

Arguments

| Name        | Type                                          | Description                                                                                |
| ----------- | --------------------------------------------- | ------------------------------------------------------------------------------------------ |
| `r`         | [`rect?`](https://lua.fatality.win/rect.html) | New clip rect.                                                                             |
| `intersect` | `bool`                                        | Whether this function should intersect previous rect with the new one. Defaults to `true`. |

Returns

Nothing.

Example

```
layer:override_clip_rect(draw.rect(50, 50, 150, 150));
```
