# adapter

This type represents a rendering adapter used within the rendering system.

### get\_back\_buffer﻿ <a href="#get-back-buffer" id="get-back-buffer"></a>

Method

Returns a back buffer texture. May return a blank or outdated texture, if the back buffer texture was not updated.

Arguments

None.

Returns

| Type                                       | Description                  |
| ------------------------------------------ | ---------------------------- |
| [`ptr`](https://lua.fatality.win/ptr.html) | Back buffer texture pointer. |

Example

```
local bb = adapter:get_back_buffer();
```

### get\_back\_buffer\_downsampled﻿ <a href="#get-back-buffer-downsampled" id="get-back-buffer-downsampled"></a>

Method

Returns a 4x down sampled version of the back buffer texture.

Arguments

None.

Returns

| Type                                       | Description                              |
| ------------------------------------------ | ---------------------------------------- |
| [`ptr`](https://lua.fatality.win/ptr.html) | Downsampled back buffer texture pointer. |

Example

```
local ds = adapter:get_back_buffer_downsampled();
```

### get\_shared\_texture﻿ <a href="#get-shared-texture" id="get-shared-texture"></a>

Method

Returns a shared texture. This texture usually replicates the down sampled back buffer texture, although it is updated automatically ONCE before the rendering on the layer starts.

Arguments

None.

Returns

| Type                                       | Description             |
| ------------------------------------------ | ----------------------- |
| [`ptr`](https://lua.fatality.win/ptr.html) | Shared texture pointer. |

Example

```
local shared = adapter:get_shared_texture();
```
