# Global Functions

Below is a list of all global functions. By “global”, we mean these functions do not require a preceding namespace - so you can call them directly, unlike other functions.

### print﻿ <a href="#print" id="print"></a>

Function

Prints text to game's console.

Arguments

| Name   | Type   | Description                     |
| ------ | ------ | ------------------------------- |
| `text` | string | String to print in the console. |

Returns

Nothing.

Example

```
print('Hello world!'); -- prints out "Hello world!" to the console
```

### error﻿ <a href="#error" id="error"></a>

Function

Prints an error text to game's console, and shuts down the script. Try to avoid using this function - use it only if an error happens which you can't recover from.

Arguments

| Name   | Type   | Description                                                                             |
| ------ | ------ | --------------------------------------------------------------------------------------- |
| `text` | string | Read [`print`](https://lua.fatality.win/global-functions.html#print) for documentation. |

Returns

Nothing.

Example

```
error('Can't recover from this one! Error: ' .. tostring(123));
```
