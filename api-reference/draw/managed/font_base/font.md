# font

This type represents a font object. Internally, this type uses FreeType library to rasterize font glyphs.

> ####
>
> This type inherits [`font_base`](https://lua.fatality.win/font-base.html) type. All of its base methods and fields are also available in this type.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs a font object.

> ####
>
> Passing an invalid pointer, a or memory region that is smaller than the size will result in a crash.

Arguments

1\. From file.

| Name   | Type                                                     | Description                                                       |
| ------ | -------------------------------------------------------- | ----------------------------------------------------------------- |
| `path` | `string`                                                 | Path to a ttf/otf file.                                           |
| `size` | `float`                                                  | Font height, in pixels.                                           |
| `fl`   | [`font_flags`](https://lua.fatality.win/font-flags.html) | Font flags. Use `bit` library to construct them. Defaults to `0`. |
| `mi`   | `int`                                                    | Starting codepoint. Defaults to `0`.                              |
| `ma`   | `int`                                                    | Ending codepoint. Defaults to `255` (entire ASCII code page).     |

1\. From memory.

| Name   | Type                                                     | Description                                                       |
| ------ | -------------------------------------------------------- | ----------------------------------------------------------------- |
| `mem`  | [`ptr`](https://lua.fatality.win/ptr.html)               | Pointer to a font file in memory.                                 |
| `sz`   | `int`                                                    | Font file size, in bytes.                                         |
| `size` | `float`                                                  | Font height, in pixels.                                           |
| `fl`   | [`font_flags`](https://lua.fatality.win/font-flags.html) | Font flags. Use `bit` library to construct them. Defaults to `0`. |
| `mi`   | `int`                                                    | Starting codepoint. Defaults to `0`.                              |
| `ma`   | `int`                                                    | Ending codepoint. Defaults to `255` (entire ASCII code page).     |

1\. From memory, with codepoint pairs.

| Name    | Type                                                     | Description                                                              |
| ------- | -------------------------------------------------------- | ------------------------------------------------------------------------ |
| `mem`   | [`ptr`](https://lua.fatality.win/ptr.html)               | Pointer to a font file in memory.                                        |
| `sz`    | `int`                                                    | Font file size, in bytes.                                                |
| `size`  | `float`                                                  | Font height, in pixels.                                                  |
| `fl`    | [`font_flags`](https://lua.fatality.win/font-flags.html) | Font flags. Use `bit` library to construct them. Defaults to `0`.        |
| `pairs` | `table[{int, int}...]`                                   | Min/max pairs. This is a standard array, consisting of {int, int} pairs. |

Returns

| Type   | Description  |
| ------ | ------------ |
| `font` | Font object. |

Example

```
local cool_font = draw.font('myfont.ttf', 16);
```
