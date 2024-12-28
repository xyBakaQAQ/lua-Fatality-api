# notification

This type represents a notification item.

### \_\_call﻿ <a href="#call" id="call"></a>

Constructor

Constructs the notification.

Arguments

| Name  | Type                                                | Description              |
| ----- | --------------------------------------------------- | ------------------------ |
| `hdr` | `string`                                            | Header (title).          |
| `txt` | `string`                                            | Text (body).             |
| `ico` | [`texture?`](https://lua.fatality.win/texture.html) | Icon. Defaults to `nil`. |

Returns

| Type           | Description          |
| -------------- | -------------------- |
| `notification` | Notification object. |

Example

```
local notif = gui.notification('Hello', 'Lua works!');
```
