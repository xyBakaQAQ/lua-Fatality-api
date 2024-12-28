# text\_params

This type is used to determine text alignment.

> ####
>
> Line alignment only makes sense if you have multiple lines in your text. By default, all next lines will start from the left side of the text. You can change this behavior by using one of the functions that take `line` as a parameter. For example, if you pass `right` to the line alignment, all next lines will start from the right side. Text alignment will remain as dictated by `v` and `h` parameters.

### with\_v﻿ <a href="#with-v" id="with-v"></a>

Function

Creates `text_params` instance with vertical alignment.

Arguments

| Name | Type                                                             | Description         |
| ---- | ---------------------------------------------------------------- | ------------------- |
| `v`  | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Vertical alignment. |

Returns

| Type          | Description          |
| ------------- | -------------------- |
| `text_params` | Created text params. |

Example

```
local align_top = draw.text_params.with_v(draw.text_alignment.top);
```

### with\_h﻿ <a href="#with-h" id="with-h"></a>

Function

Creates `text_params` instance with horizontal alignment.

Arguments

| Name | Type                                                             | Description           |
| ---- | ---------------------------------------------------------------- | --------------------- |
| `h`  | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Horizontal alignment. |

Returns

| Type          | Description          |
| ------------- | -------------------- |
| `text_params` | Created text params. |

Example

```
local align_right = draw.text_params.with_h(draw.text_alignment.right);
```

### with\_line﻿ <a href="#with-line" id="with-line"></a>

Function

Creates `text_params` instance with line alignment.

Arguments

| Name   | Type                                                             | Description     |
| ------ | ---------------------------------------------------------------- | --------------- |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Line alignment. |

Returns

| Type          | Description          |
| ------------- | -------------------- |
| `text_params` | Created text params. |

Example

```
local lines_center = draw.text_params.with_line(draw.text_alignment.center);
```

### with\_vh﻿ <a href="#with-vh" id="with-vh"></a>

Function

Creates `text_params` instance with vertical and horizontal alignments.

Arguments

| Name | Type                                                             | Description           |
| ---- | ---------------------------------------------------------------- | --------------------- |
| `v`  | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Vertical alignment.   |
| `h`  | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Horizontal alignment. |

Returns

| Type          | Description          |
| ------------- | -------------------- |
| `text_params` | Created text params. |

Example

```
local align_bottom_right = draw.text_params.with_vh(draw.text_alignment.bottom, draw.text_alignment.right);
```

### with\_vline﻿ <a href="#with-vline" id="with-vline"></a>

Function

Creates `text_params` instance with vertical alignment and line alignment.

Arguments

| Name   | Type                                                             | Description         |
| ------ | ---------------------------------------------------------------- | ------------------- |
| `v`    | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Vertical alignment. |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Line alignment.     |

Returns

| Type          | Description          |
| ------------- | -------------------- |
| `text_params` | Created text params. |

Example

```
local align = draw.text_params.with_vline(draw.text_alignment.bottom, draw.text_alignment.center);
```

### with\_hline﻿ <a href="#with-hline" id="with-hline"></a>

Function

Creates `text_params` instance with horizontal alignment and line alignment.

Arguments

| Name   | Type                                                             | Description           |
| ------ | ---------------------------------------------------------------- | --------------------- |
| `h`    | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Horizontal alignment. |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Line alignment.       |

Returns

| Type          | Description          |
| ------------- | -------------------- |
| `text_params` | Created text params. |

Example

```
local align = draw.text_params.with_hline(draw.text_alignment.center, draw.text_alignment.center);
```

### with\_vhline﻿ <a href="#with-vhline" id="with-vhline"></a>

Function

Creates `text_params` instance with vertical, horizontal and line alignments.

Arguments

| Name   | Type                                                             | Description           |
| ------ | ---------------------------------------------------------------- | --------------------- |
| `v`    | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Vertical alignment.   |
| `h`    | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Horizontal alignment. |
| `line` | [`text_alignment`](https://lua.fatality.win/text-alignment.html) | Line alignment.       |

Returns

| Type          | Description          |
| ------------- | -------------------- |
| `text_params` | Created text params. |

Example

```
local align = draw.text_params.with_vhline(draw.text_alignment.center, draw.text_alignment.center
```
