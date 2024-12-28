# animated\_texture

This type is an animated texture. This texture type only supports animated GIF types, and does not support APNG.

> ####
>
> This type inherits [`texture`](https://lua.fatality.win/texture.html) type. All of its base methods and fields are also available in this type.

> ####
>
> If you pass an unsupported type, it will instead work exactly like [`texture`](https://lua.fatality.win/texture.html) type, meaning controlling frames and looping will be meaningless.

> ####
>
> Using this type for texture atlases is possible, although highly unrecommended. It will produce extra texture objects in memory, and overall will be much slower. Instead, it is advised to construct an actual texture atlas, use [`texture`](https://lua.fatality.win/texture.html) type, and use texture mapping.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs animated texture.

> ####
>
> Passing an invalid pointer, a or memory region that is smaller than the size will result in a crash.

Arguments

1\. From file.

| Name   | Type     | Description               |
| ------ | -------- | ------------------------- |
| `path` | `string` | Path to the texture file. |

2\. From memory.

| Name   | Type                                       | Description                             |
| ------ | ------------------------------------------ | --------------------------------------- |
| `data` | [`ptr`](https://lua.fatality.win/ptr.html) | Pointer to texture file data in memory. |
| `sz`   | `int`                                      | Size of the texture file data.          |

Returns

| Type               | Description                |
| ------------------ | -------------------------- |
| `animated_texture` | Animated texture instance. |

Example

```
local gif = draw.animated_texture('funny_gif.gif');
```

### should\_loop﻿ <a href="#should-loop" id="should-loop"></a>

Field

Type: `bool`

If set to `false`, will not loop the animation automatically. Defaults to `true`.

### reset\_loop﻿ <a href="#reset-loop" id="reset-loop"></a>

Method

Reset loop to run from the first frame.

Arguments

None.

Returns

Nothing.

Example

```
gif:reset_loop();
```

### set\_frame﻿ <a href="#set-frame" id="set-frame"></a>

Method

Set a specific frame on the animation. If looping is enabled, will continue the cycle from the passed frame. Otherwise, will display a specific frame of the animation.

> ####
>
> Frame count starts from `0`.

Arguments

| Name    | Type  | Description                                          |
| ------- | ----- | ---------------------------------------------------- |
| `frame` | `int` | Frame number. Invalid frame numbers will be clamped. |

Returns

Nothing.

Example

```
gif:set_frame(5);
```

### get\_frame\_count﻿ <a href="#get-frame-count" id="get-frame-count"></a>

Method

Returns amount of frames in the animation.

Arguments

None.

Returns

| Type  | Description  |
| ----- | ------------ |
| `int` | Frame count. |

Example

```
local frames = gif:get_frame_count();
gif:set_frame(frames - 2); -- set to the last frame
```
