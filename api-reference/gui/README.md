# gui

Usage:

`gui.{func_or_field}`

This table exposes the GUI system of the software.

> ####
>
> All types and enums described in the child sections must be prefixed with `gui.`.

### ctx﻿ <a href="#ctx" id="ctx"></a>

Field

Type: [`context`](https://lua.fatality.win/context.html)

GUI context.

### notify﻿ <a href="#notify" id="notify"></a>

Field

Type: [`notification_system`](https://lua.fatality.win/notification-system.html)

Notification system.

### make\_control﻿ <a href="#make-control" id="make-control"></a>

Function

Wraps a control into a layout consisting of a label and that specific control. You should add this new control to groupboxes if you want your control to be displayed nicely. Additionally, you can add any extra controls to the returned one - those will get stacked to the left side of your initial control.

Arguments

| Name   | Type                                               | Description     |
| ------ | -------------------------------------------------- | --------------- |
| `text` | `string`                                           | Label value.    |
| `c`    | [`control`](https://lua.fatality.win/control.html) | Control object. |

Returns

| Type                                             | Description    |
| ------------------------------------------------ | -------------- |
| [`layout`](https://lua.fatality.win/layout.html) | Layout object. |

Example

```
local row = gui.make_control('Hello checkbox!', my_cb);
```
