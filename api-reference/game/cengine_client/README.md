# cengine\_client

Usage:

`game.engine.{method}`

An instance of this type provides a way to interface with Source 2's Engine-to-Client service.

### get\_last\_timestamp﻿ <a href="#get-last-timestamp" id="get-last-timestamp"></a>

Method

Returns last timestamp, in seconds.

Arguments

None.

Returns

| Type    | Description            |
| ------- | ---------------------- |
| `float` | Timestamp, in seconds. |

Example

```
local last_time = game.engine:get_last_timestamp();
```

### get\_last\_server\_tick﻿ <a href="#get-last-server-tick" id="get-last-server-tick"></a>

Method

Returns last server tick number.

Arguments

None.

Returns

| Type  | Description         |
| ----- | ------------------- |
| `int` | Server tick number. |

Example

```
local server_tick = game.engine:get_last_server_tick();
```

### in\_game﻿ <a href="#in-game" id="in-game"></a>

Method

Returns whether the client is currently in game.

Arguments

None.

Returns

| Type   | Description     |
| ------ | --------------- |
| `bool` | In-game status. |

Example

```
if game.engine:in_game() then
    print("I'm in game!");
end
```

### is\_connected﻿ <a href="#is-connected" id="is-connected"></a>

Method

Returns whether the client is currently connected to a game server.

Arguments

None.

Returns

| Type   | Description          |
| ------ | -------------------- |
| `bool` | `true` if connected. |

Example

```
if game.engine:is_connected() then
    print("I'm connected!");
end
```

### get\_netchan﻿ <a href="#get-netchan" id="get-netchan"></a>

Method

Returns the Network Channel used for network communication.

Arguments

None.

Returns

| Type                                                   | Description                                  |
| ------------------------------------------------------ | -------------------------------------------- |
| [`cnet_chan`](https://lua.fatality.win/cnet-chan.html) | Network channel, or `nil` if does not exist. |

Example

```
local chan = game.engine:get_netchan();
```

### client\_cmd﻿ <a href="#client-cmd" id="client-cmd"></a>

Method

Executes a client-sided console command.

Arguments

| Name   | Type           | Description                                                                  |
| ------ | -------------- | ---------------------------------------------------------------------------- |
| `cmd`  | `string`       | Command to execute.                                                          |
| `bool` | `unrestricted` | Whether should the execution preserve any restrictions. Defaults to `false`. |

Returns

Nothing.

Example

```
game.engine:client_cmd('say Hello!');
```

### get\_screen\_size﻿ <a href="#get-screen-size" id="get-screen-size"></a>

Method

Returns client window screen size.

Arguments

None.

Returns

| Type  | Description |
| ----- | ----------- |
| `int` | Width.      |
| `int` | Height.     |

Example

```
local w, h = game.engine:get_screen_size();
```
