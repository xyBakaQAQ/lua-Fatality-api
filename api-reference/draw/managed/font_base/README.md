# font\_base

This type represents the base class for font types. You cannot create an instance of this type. Instead, use the children types.

> ####
>
> This type inherits [`managed`](https://lua.fatality.win/managed.html) type. All of its base methods and fields are also available in this type.

> ####
>
> Definitions:
>
> * codepoint: Unicode representation of the character.
> * kerning: a distance between two characters.
> * glyph: visual representation of a character.

### height﻿ <a href="#height" id="height"></a>

FieldRead Only

Type: `float`

Font height, in pixels.

### ascent﻿ <a href="#ascent" id="ascent"></a>

Field

Type: `float`

Font ascent value, in pixels.

### descent﻿ <a href="#descent" id="descent"></a>

Field

Type: `float`

Font descent value, in pixels.

### line\_gap﻿ <a href="#line-gap" id="line-gap"></a>

Field

Type: `float`

Font line gap, in pixels.

### kerning\_gap﻿ <a href="#kerning-gap" id="kerning-gap"></a>

Field

Type: `float`

Font kerning gap, in pixels.

### outline\_alpha﻿ <a href="#outline-alpha" id="outline-alpha"></a>

Field

Type: `float`

Font outline opacity (`0` to `1`). Defaults to `0.45`.

### flags﻿ <a href="#flags" id="flags"></a>

FieldRead Only

Type: [`font_flags`](https://lua.fatality.win/font-flags.html)

Font flags. Use `bit` library to read flags.

### y\_offset﻿ <a href="#y-offset" id="y-offset"></a>

Field

Type: `int`

Glyph Y offset, in pixels. Will alter the location of a glyph in the atlas. Changing this value after the font was created is meaningless.

### x\_offset﻿ <a href="#x-offset" id="x-offset"></a>

Field

Type: `int`

Glyph X offset, in pixels. Will alter the location of a glyph in the atlas. Changing this value after the font was created is meaningless.

### fallback\_font﻿ <a href="#fallback-font" id="fallback-font"></a>

Field

Type: `font_base`

Fallback font to use, in case a glyph is not found in this font. Is it useful when one font does not have codepoints for specific symbols, that are present in another font, but you still want to prefer this font's glyphs over other font.

### dropshadow\_color﻿ <a href="#dropshadow-color" id="dropshadow-color"></a>

Field

Type: [`color`](https://lua.fatality.win/rcolor.html)

Shadow color. Only R, G, B values are used.

### get\_kerned\_char\_width﻿ <a href="#get-kerned-char-width" id="get-kerned-char-width"></a>

Method

Returns character width, included with kerning.

Arguments

| Name    | Type  | Description                   |
| ------- | ----- | ----------------------------- |
| `left`  | `int` | Previous character codepoint. |
| `right` | `int` | Current character codepoint.  |

Returns

| Type    | Description          |
| ------- | -------------------- |
| `float` | Distance, in pixels. |

Example

```
local w = font:get_kerned_char_width(prev_cp, cp);
```

### get\_kerning﻿ <a href="#get-kerning" id="get-kerning"></a>

Method

Returns kerning value for a single character. If kerning is disabled, will instead return kerning gap.

Arguments

| Name | Type  | Description |
| ---- | ----- | ----------- |
| `cp` | `int` | Codepoint.  |

Returns

| Type    | Description               |
| ------- | ------------------------- |
| `float` | Kerning value, in pixels. |

Example

```
local k = font:get_kerning(cp);
```

### get\_text\_size﻿ <a href="#get-text-size" id="get-text-size"></a>

Method

Returns text area size.

Arguments

| Name           | Type     | Description                                                          |
| -------------- | -------- | -------------------------------------------------------------------- |
| `text`         | `string` | Text.                                                                |
| `skip_scaling` | `bool`   | If set to `true`, will skip global DPI scaling. Defaults to `false`. |
| `til_newline`  | `bool`   | Calculate size only until a line break is met. Defaults to `false`.  |

Returns

| Type                                         | Description     |
| -------------------------------------------- | --------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Text area size. |

Example

```
local sz = font:get_text_size('Hello!');
```

### wrap\_text﻿ <a href="#wrap-text" id="wrap-text"></a>

Method

Wraps text to meet the desired width. Wrapping is done by breaking text by words and inserting line breaks in between. If one of the words is longer than the target width, will instead use that word's width.

Arguments

| Name    | Type     | Description   |
| ------- | -------- | ------------- |
| `text`  | `string` | Text to wrap. |
| `width` | `float`  | Target width. |

Returns

| Type     | Description   |
| -------- | ------------- |
| `string` | Wrapped text. |

Example

```
local shorter = font:wrap_text('This is some very long text!', 50);
```

### get\_glyph﻿ <a href="#get-glyph" id="get-glyph"></a>

Method

Returns glyph information for a character.

Arguments

| Name        | Type  | Description |
| ----------- | ----- | ----------- |
| `codepoint` | `int` | Codepoint.  |

Returns

| Type                                               | Description        |
| -------------------------------------------------- | ------------------ |
| [`glyph_t`](https://lua.fatality.win/glyph-t.html) | Glyph information. |

Example

```
local glyph = font:get_glyph(cp);
```

### get\_texture﻿ <a href="#get-texture" id="get-texture"></a>

Method

Returns a texture atlas that contains the provided glyph.

Arguments

| Name | Type                                               | Description      |
| ---- | -------------------------------------------------- | ---------------- |
| `gl` | [`glyph_t`](https://lua.fatality.win/glyph-t.html) | Character glyph. |

Returns

| Type  | Description                             |
| ----- | --------------------------------------- |
| `int` | Texture pointer, or `nil` if not found. |

Example

```
local atlas = font:get_texture(glyph);
```
