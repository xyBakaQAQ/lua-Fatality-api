# command

This type is used to change render command parameters.

> ####
>
> Be cautious when changing stuff in an instance of this type. Passing invalid data to `texture` or `frag_shader`, or not restoring some changes after you're done drawing can lead to undefined behavior, and more likely, a crash. If you are not sure how to operate this type, take a look into examples.

### texture﻿ <a href="#texture" id="texture"></a>

Field

Type: [`ptr`](https://lua.fatality.win/ptr.html)

Texture pointer. You can get one from an instance of `texture` type by accessing `obj` field. Passing invalid data to this field WILL result in a crash. For a safer way, please use [`set_texture`](https://lua.fatality.win/command.html#set-texture).

### frag\_shader﻿ <a href="#frag-shader" id="frag-shader"></a>

Field

Type: Type: [`ptr`](https://lua.fatality.win/ptr.html)

Fragment shader (aka Pixel Shader in DirectX terms) pointer. You can get one from an instance of `shader` type by accessing `obj` field. Passing invalid data to this field WILL result in a crash. For a safer way, please use [`set_shader`](https://lua.fatality.win/command.html#set-shader).

### clip\_rect﻿ <a href="#clip-rect" id="clip-rect"></a>

Field

Type: [`rect?`](https://lua.fatality.win/rect.html)

Clip rectangle used for scissor testing. If this is set to `nil`, will not clip anything.

> ####
>
> It is advised to instead use layer's `override_clip_rect` method. While you can pass custom rect to this field, you will lose information about previous clip rects set before. Using that method will make sure to intersect the previous rect with the one you pass and produce a probably more expected result.

### uv\_rect﻿ <a href="#uv-rect" id="uv-rect"></a>

Field

Type: [`rect?`](https://lua.fatality.win/rect.html)

UV rect used for texture mapping. If this field is set to `nil`, will use `0, 0, 1, 1` rectangle to map the texture. You can learn more about texture mapping in the tutorial section.

### alpha﻿ <a href="#alpha" id="alpha"></a>

Field

Type: `float`

Global opacity override. Defaults to `1`, but if you set anything else - will modulate opacity of every next shape you will render.

### rotation﻿ <a href="#rotation" id="rotation"></a>

Field

Type: `float`

Shape rotation. Not all shapes support this field. The value is set in degrees, not radians.

### anti\_alias﻿ <a href="#anti-alias" id="anti-alias"></a>

Field

Type: `bool`

If set to `true`, will apply tesselation to shapes.

> ####
>
> As of now, not every shape supports tesselation, but it is advised to have it enabled at all times anyway. It will produce much better result anyway.

### ignore\_scaling﻿ <a href="#ignore-scaling" id="ignore-scaling"></a>

Field

Type: `bool`

If set to `true`, will ignore global DPI scale. This is set to `true` by default, but you are free to change it to `false` if you are trying to render some custom UI elements.

### chained\_call﻿ <a href="#chained-call" id="chained-call"></a>

Field

Type: `bool`

Only useful when using shaders. If set to `true`, will not update back buffer texture. This can be used if you need the very same texture data, as when applying several shaders to the back buffer.

> ####
>
> Please note that capturing back buffer is a rather slow operation. It is better to not capture it too often. Back buffer is automatically captured to the only layer you can use anyway, and it is better to use that one instead, to make sure rendering happens as fast as it is possible.

### only\_downsampled﻿ <a href="#only-downsampled" id="only-downsampled"></a>

Field

Type: `bool`

If set to `true`, will capture back buffer (as long as `chained_call` is set to `false`). The name of this field is quite misleading due to the fact that in the CS:GO version of Fatality, it was used to configure if the rendering system should also downsample the captured backbuffer into another texture. In DirectX11, this operation is much faster, so it is done regardless.

### capture\_back\_buffer﻿ <a href="#capture-back-buffer" id="capture-back-buffer"></a>

Field

Type: `bool`

An alias to `only_downsampled`.

### is\_tile﻿ <a href="#is-tile" id="is-tile"></a>

Field

Type: `bool`

If set to `true`, will use a separate texture sampler that supports tiling. By default, all textures are stretched, but if you enable this option - their tiling and stretch will be fully configurable by the `uv_rect` field.

### mode﻿ <a href="#mode" id="mode"></a>

Field

Type: [`render_mode`](https://lua.fatality.win/render-mode.html)

Rendering mode. You can read more about it in the type's documentation.

### set\_texture﻿ <a href="#set-texture" id="set-texture"></a>

Method

Sets a texture in a safe manner.

Arguments

| Name  | Type                                               | Description     |
| ----- | -------------------------------------------------- | --------------- |
| `tex` | [`texture`](https://lua.fatality.win/texture.html) | Texture object. |

Returns

Nothing.

Example

```
cmd:set_texture(my_tex);
```

### set\_shader﻿ <a href="#set-shader" id="set-shader"></a>

Method

Sets a fragment shader in a safe manner.

Arguments

| Name | Type        | Description    |
| ---- | ----------- | -------------- |
| `sh` | \[`shader`] | Shader object. |

Returns

Nothing.

Example

```
cmd:set_shader(my_shader);
```
