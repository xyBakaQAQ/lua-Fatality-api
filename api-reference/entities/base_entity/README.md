# base\_entity

This type represents a base game entity.

> ####
>
> This type may be returned for any other abstract entity class, but internally will point to the correct type.

### \_\_index﻿ <a href="#index" id="index"></a>

Function

Attemps to search for a field in this class.

Arguments

| Name   | Type     | Description |
| ------ | -------- | ----------- |
| `name` | `string` | Field name. |

Returns

| Type                                                                   | Description        |
| ---------------------------------------------------------------------- | ------------------ |
| [`schema_accessor_t`](https://lua.fatality.win/schema-accessor-t.html) | Accessor instance. |

Example

```
local health = player.m_iHealth;
local health = player['m_iHealth']; -- this also works
```
