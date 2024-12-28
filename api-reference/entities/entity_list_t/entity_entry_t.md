# entity\_entry\_t

Represents an entity entry.

### entity﻿ <a href="#entity" id="entity"></a>

Field

Type: `<type>`

Entity instance. Type depends on the list you get it from.

### had\_dataupdate﻿ <a href="#had-dataupdate" id="had-dataupdate"></a>

Field

Type: `bool`

`true` if the client had received any updates to this entity at least once.

### handle﻿ <a href="#handle" id="handle"></a>

Field

Type: [`chandle<type>`](https://lua.fatality.win/chandle.html)

Entity's handle. You may store this elsewhere if you need to have global access to an entity.

### avatar﻿ <a href="#avatar" id="avatar"></a>

Field

Type: [`texture`](https://lua.fatality.win/texture.html)

> ####
>
> This field is only available on entries that use `cs2_player_controller` type.

Player's profile picture. Will be `nil` if was yet to be initialized.
