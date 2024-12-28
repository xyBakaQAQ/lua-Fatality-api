# entity\_list\_t

This type represents an entity list.

> ####
>
> Never save any entities you get from this list if you don't know what you are doing! You may be left with dangling pointers, which will inevitably lead to a crash.

### for\_each﻿ <a href="#for-each" id="for-each"></a>

Method

Loops the entities.

Arguments

| Name | Type                       | Description        |
| ---- | -------------------------- | ------------------ |
| `fn` | `function(entity_entry_t)` | Function callback. |

Returns

Nothing.

Example

```
entities.players:for_each(function (entry)
    -- ...
end);
```

### for\_each\_z﻿ <a href="#for-each-z" id="for-each-z"></a>

Method

Loops the entities in the reverse order.

Arguments

| Name | Type                       | Description        |
| ---- | -------------------------- | ------------------ |
| `fn` | `function(entity_entry_t)` | Function callback. |

Returns

Nothing.

Example

```
entities.players:for_each_z(function (entry)
    -- ...
end);
```
