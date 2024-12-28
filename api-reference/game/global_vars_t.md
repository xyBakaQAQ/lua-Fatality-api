# global\_vars\_t

Usage:

`game.global_vars.{field}`

An instance of this type provides a way to read several global variables that are used by the game. Changing any of the values is not and will never be supported.

### real\_time﻿ <a href="#real-time" id="real-time"></a>

Field

Type: `float`

Time passed since the game start, in seconds.

### frame\_count﻿ <a href="#frame-count" id="frame-count"></a>

Field

Type: `int`

Amount of frames rendered since the game start.

### abs\_frame\_time﻿ <a href="#abs-frame-time" id="abs-frame-time"></a>

Field

Type: `float`

Absolute (averaged) frame time. It is calculated over a set of previous frame times, and should not be used for anything that requires accurate frame time like animation.

### max\_clients﻿ <a href="#max-clients" id="max-clients"></a>

Field

Type: `int`

Maximum amount of clients on the current server.

### ticks\_this\_frame﻿ <a href="#ticks-this-frame" id="ticks-this-frame"></a>

Field

Type: `int`

Amount of ticks passed during the currently rendered frame. Any value above 1 might indicate a stall during rendering.

### frame\_time﻿ <a href="#frame-time" id="frame-time"></a>

Field

Type: `float`

Time, in which a previous frame was rendered. May be used for animation or by any other means that require accurate frame time.

### cur\_time﻿ <a href="#cur-time" id="cur-time"></a>

Field

Type: `float`

Time passed since the server's game start. This does not indicate the accurate time on the server, although in several events it might be synced by the software.

### tick\_fraction﻿ <a href="#tick-fraction" id="tick-fraction"></a>

Field

Type: `float`

Current tick's fractional value.

### tick\_count﻿ <a href="#tick-count" id="tick-count"></a>

Field

Type: `int`

Ticks passed since the server's game start.

### map\_path﻿ <a href="#map-path" id="map-path"></a>

Field

Type: `string`

Relative path to current loaded map's file.

### map\_name﻿ <a href="#map-name" id="map-name"></a>

Field

Type: `string`

Name of the currently loaded map.
