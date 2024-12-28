# font\_gdi

This type represents a font object. Internally, this type uses GDI library to rasterize font glyphs.

> ####
>
> This type inherits [`font_base`](https://lua.fatality.win/font-base.html) type. All of its base methods and fields are also available in this type.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs a font object.

Arguments

| Name     | Type                                                     | Description                                                       |
| -------- | -------------------------------------------------------- | ----------------------------------------------------------------- |
| `name`   | `string`                                                 | System font name (example: 'Arial').                              |
| `size`   | `float`                                                  | Font height, in pixels.                                           |
| `fl`     | [`font_flags`](https://lua.fatality.win/font-flags.html) | Font flags. Use `bit` library to construct them. Defaults to `0`. |
| `mi`     | `int`                                                    | Starting codepoint. Defaults to `0`.                              |
| `ma`     | `int`                                                    | Ending codepoint. Defaults to `255` (entire ASCII code page).     |
| `weight` | `int`                                                    | Font weight. Defaults to `400` (regular).                         |

Returns

| Type       | Description  |
| ---------- | ------------ |
| `font_gdi` | Font object. |

Example

```
local sys_font = draw.font_gdi('Calibri', 14);
```

* \
