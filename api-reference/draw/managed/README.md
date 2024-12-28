# managed

This type represents a managed object. You cannot create an instance of this type directly.

Every object, that inherits from this type, must be `create`d before use. The rendering system will only create them automatically, if you happen to lose a device object (e.g. minimize the game window, and then restore it) and only if you add your objects to manage table in [`draw`](https://lua.fatality.win/draw.html).

### obj﻿ <a href="#obj" id="obj"></a>

FieldRead Only

Type: [`ptr`](https://lua.fatality.win/ptr.html)

Pointer to a GPU object. If this object is not created, this field will be `nil`. You can use the value of this field to pass it to [`command`](https://lua.fatality.win/command.html) directly for example, or if you (for whatever reason we don't recommend you doing) want to have a direct control over the pointer - cast it to FFI's `cdata`.

### create﻿ <a href="#create" id="create"></a>

Method

Creates a managed object in GPU memory.

> ####
>
> You should `create()` an object only once. Invoking this method after the object was created will be meaningless.

Arguments

None.

Returns

Nothing.

Example

```
tex:create();
```

### destroy﻿ <a href="#destroy" id="destroy"></a>

Method

Destroys a managed object in GPU memory.

> ####
>
> Never destroy a GPU object if it is being used in rendering (for example, when you have pushed some shape that uses a texture, and then destroyed that texture). This will lead to undefined behavior, and most likely, \*\*crash the game \*\*.

Arguments

None.

Returns

Nothing.

Example

```
font:destroy();
```
