# cnet\_chan

Provides a way to interface with a Network Channel's class.

### get\_address﻿ <a href="#get-address" id="get-address"></a>

Method

> ####
>
> If the current channel is `null`, this function will return `nil` instead.

Returns address string of the remote machine.

Arguments

None.

Returns

| Type      | Description                         |
| --------- | ----------------------------------- |
| `string?` | IP-address or Steam Server Address. |

Example

```
local chan = game.engine:get_netchan();
if chan and not chan:is_null() then
    print(chan:get_address());
end
```

### is\_loopback﻿ <a href="#is-loopback" id="is-loopback"></a>

Method

> ####
>
> If the current channel is `null`, this function will return `nil` instead.

Returns whether the current channel is connected to the local machine (loopback address).

Arguments

None.

Returns

| Type    | Description                               |
| ------- | ----------------------------------------- |
| `bool?` | `true` if connected to the local machine. |

Example

```
local chan = game.engine:get_netchan();
if chan and not chan:is_null() and chan:is_loopback() then
    print('Connected to localhost!');
end
```

### is\_null﻿ <a href="#is-null" id="is-null"></a>

Method

Returns whether the channel is stubbed.

Arguments

None.

Returns

| Type   | Description                                   |
| ------ | --------------------------------------------- |
| `bool` | `true` if current channel is a dummy channel. |

Example

```
local chan = game.engine:get_netchan();
if not chan or chan:is_null() then
    print('Not connected!');
end
```

### get\_latency﻿ <a href="#get-latency" id="get-latency"></a>

Method

> ####
>
> If the current channel is `null`, this function will return `nil` instead.

Returns current latency to the remote server (in seconds).

Arguments

None.

Returns

| Type     | Description           |
| -------- | --------------------- |
| `float?` | Latency (in seconds). |

Example

```
local chan = game.engine:get_netchan();
if chan and not chan:is_null() then
    print('Current latency: ' .. tostring(math.round(chan:get_latency() * 1000.0)) .. 'ms');
end
```
