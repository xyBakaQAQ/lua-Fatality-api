# event\_t

Event usertype. An instance of this type can be found in [`events`](https://lua.fatality.win/events.html).

### add﻿ <a href="#add" id="add"></a>

Method

Adds a callback to the event.

Arguments

| Name | Type       | Description                                                                                        |
| ---- | ---------- | -------------------------------------------------------------------------------------------------- |
| `fn` | `function` | Callback function. Arguments that are accepted by the function are dictated by the event instance. |

Returns

Nothing.

Example

```
events.present_queue:add(function ()
    -- will be called every time game queues a frame for rendering
end);
```

### remove﻿ <a href="#remove" id="remove"></a>

Method

Removes a callback from the event.

Arguments

| Name | Type       | Description                                                         |
| ---- | ---------- | ------------------------------------------------------------------- |
| `fn` | `function` | Callback function, that was earlier passed to the `add()` function. |

Returns

Nothing.

Example

```
local function on_present()
    if some_condition then
        events.present_queue:remove(on_present)
    end
end

events.present_queue:add(on_present)
```
