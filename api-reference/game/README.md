# game

Usage:

`game.{interface_or_function}`

This table exposes various internal services and global objects used by Fatality, and also provides a way to retrieve any additional services you need.

### global\_vars﻿ <a href="#global-vars" id="global-vars"></a>

Field

Type: [`global_vars_t`](https://lua.fatality.win/global-vars-t.html)

This service exposes global variables used by the game, such as frame time or current server time.

### engine﻿ <a href="#engine" id="engine"></a>

Field

Type: [`cengine_client`](https://lua.fatality.win/cengine-client.html)

This service exposes the engine client, which includes commonly used engine-related functions.
