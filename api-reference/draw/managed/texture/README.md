# texture

This type represents a texture object.

> ####
>
> This type inherits [`managed`](https://lua.fatality.win/managed.html) type. All of its base methods and fields are also available in this type.

> ####
>
> Supported texture formats are:
>
> * JPEG (.jpg, .jpeg) - 12 bpc/arithmetic are not supported.
> * PNG (.png)
> * TGA (.tga)
> * BMP (.bmp) - 1 bpp and RLE variants are not supported.
> * PSD (.psd) - composited view only, no extra channels, 8/16 bpc
> * GIF (.gif) - only first frame, for animated gifs use [`animated_texture`](https://lua.fatality.win/animated-texture.html)
> * HDR (.hdr)
> * PIC (.pic)
> * PNM (.pnm, .ppm, .pgm) - PPM and PGM are binary only

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs an instance of this type.

> ####
>
> Passing an invalid pointer, a or memory region that is smaller than the size will result in a crash.

Arguments

1\. From file.

| Name   | Type     | Description                   |
| ------ | -------- | ----------------------------- |
| `path` | `string` | Path to a valid texture file. |

2\. From memory.

| Name   | Type                                       | Description                             |
| ------ | ------------------------------------------ | --------------------------------------- |
| `data` | [`ptr`](https://lua.fatality.win/ptr.html) | Pointer to texture file data in memory. |
| `sz`   | `int`                                      | Size of the texture file data.          |

3\. From RGBA data.

| Name   | Type                                       | Description                                             |
| ------ | ------------------------------------------ | ------------------------------------------------------- |
| `data` | [`ptr`](https://lua.fatality.win/ptr.html) | Pointer to RGBA data in memory.                         |
| `w`    | `int`                                      | Width.                                                  |
| `h`    | `int`                                      | Height (row count).                                     |
| `p`    | `int`                                      | Pitch (row width). This is the amount of bytes per row. |

Returns

| Type      | Description     |
| --------- | --------------- |
| `texture` | Texture object. |

Example

```
local tex = draw.texture('funny_meme.png');
```

### is\_animated﻿ <a href="#is-animated" id="is-animated"></a>

FieldRead Only

Type: `bool`

Set to `true` if this is an instance of [`animated_texture`](https://lua.fatality.win/animated-texture.html).

### get\_size﻿ <a href="#get-size" id="get-size"></a>

Method

Returns size of this texture.

Arguments

None.

Returns

| Type                                         | Description         |
| -------------------------------------------- | ------------------- |
| [`vec2`](https://lua.fatality.win/vec2.html) | Texture dimensions. |

Example

```
local sz = tex:get_size();
```
