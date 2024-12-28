# bits

This type represents a bitset value.

> ####
>
> Maximal bit number for this type is 63. Setting or getting any bits outside of that range will cause a crash.

### reset﻿ <a href="#reset" id="reset"></a>

Method

Resets the value.

Arguments

None.

Returns

Nothing.

Example

```
bits:reset();
```

### get\_raw﻿ <a href="#get-raw" id="get-raw"></a>

Method

Returns the raw value.

Arguments

None.

Returns

| Type  | Description |
| ----- | ----------- |
| `int` | Raw value.  |

Example

```
local raw = bits:get_raw();
```

### set\_raw﻿ <a href="#set-raw" id="set-raw"></a>

Method

Sets the raw value.

Arguments

| Name  | Type  | Description |
| ----- | ----- | ----------- |
| `val` | `int` | Raw value.  |

Returns

Nothing.

Example

```
bits:set_raw(long_long_value);
```

### none﻿ <a href="#none" id="none"></a>

Method

Returns `true` if no bits are set.

Arguments

None.

Returns

| Type   | Description                |
| ------ | -------------------------- |
| `bool` | `true` if no bits are set. |

Example

```
if bits:none() then
    -- ...
end
```

### set﻿ <a href="#set" id="set"></a>

Method

Enables a bit.

Arguments

| Name  | Type  | Description |
| ----- | ----- | ----------- |
| `bit` | `int` | Bit number. |

Returns

Nothing.

Example

```
bits:set(5); -- set bit #5 (same as bit.bor(val, bit.lshift(1, 5)))
```

### unset﻿ <a href="#unset" id="unset"></a>

Method

Disables a bit.

Arguments

| Name  | Type  | Description |
| ----- | ----- | ----------- |
| `bit` | `int` | Bit number. |

Returns

Nothing.

Example

```
bits:unset(5);
```

### get﻿ <a href="#get" id="get"></a>

Method

Returns bit state.

Arguments

| Name  | Type  | Description |
| ----- | ----- | ----------- |
| `bit` | `int` | Bit number. |

Returns

| Type   | Description |
| ------ | ----------- |
| `bool` | Bit status. |

Example

```
if bits:get(5) then
    -- ...
end
```

### toggle﻿ <a href="#toggle" id="toggle"></a>

Method

Toggles bit state.

Arguments

| Name  | Type  | Description |
| ----- | ----- | ----------- |
| `bit` | `int` | Bit number. |

Returns

Nothing.

Example

```
bits:toggle(5);
```
