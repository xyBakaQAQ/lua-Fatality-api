# draw

Usage:

`draw.{func_or_field}`

This table describes the rendering system of the software.

> ####
>
> All types and enums described in the child sections must be prefixed with `draw.`. This is done so specific types are not confused with others, such as the separate `color` types present in rendering and the game.

### adapter﻿ <a href="#adapter" id="adapter"></a>

FieldRead Only

Type: [`adapter`](https://lua.fatality.win/adapter.html)

Rendering adapter.

### frame\_time﻿ <a href="#frame-time" id="frame-time"></a>

FieldRead Only

Type: `float`

Rendering frame time. An alias to [`global_vars_t.frame_time`](https://lua.fatality.win/global-vars-t.html#frame-time).

### time﻿ <a href="#time" id="time"></a>

FieldRead Only

Type: `float`

Time, in seconds. An alias to [`global_vars_t.real_time`](https://lua.fatality.win/global-vars-t.html#real-time).

### scale﻿ <a href="#scale" id="scale"></a>

FieldRead Only

Type: `float`

Global DPI scale.

### display﻿ <a href="#display" id="display"></a>

FieldRead Only

Type: [`vec2`](https://lua.fatality.win/vec2.html)

Display area size (viewport dimensions). [`cengine_client:get_screen_size`](https://lua.fatality.win/cengine-client.html#get-screen-size) will return exactly the same values. Overriding any of this vector's values will lead to an undefined behavior.

### textures﻿ <a href="#textures" id="textures"></a>

FieldRead Only

Type: [`accessor<texture>`](https://lua.fatality.win/accessor.html)

A string to [`texture`](https://lua.fatality.win/texture.html) map of all managed textures. You can query and push textures with custom IDs. When you add a texture to this map, it will be automatically destroyed and recreated when required (such as when DX11 device gets lost).

> ####
>
> Built-in textures:
>
> * `gui_loading`: loading spinner
> * `gui_user_avatar`: current user's profile picture. May be `nil` if you don't have any avatar set
> * `gui_icon_up`: up chevron
> * `gui_icon_down`: down chevron
> * `gui_icon_copy`: copy icon
> * `gui_icon_paste`: paste icon
> * `gui_icon_add`: add icon
> * `gui_icon_search`: search icon
> * `gui_icon_settings`: settings icon (a cogwheel)
> * `gui_icon_bug`: bug icon
> * `gui_icon_key.N`: keyboard/mouse key icons. Replace `N` with the char code of a required button
> * `icon_rage`: RAGE tab icon
> * `icon_legit`: LEGIT tab icon
> * `icon_visuals`: VISUALS tab icon
> * `icon_misc`: MISC tab icon
> * `icon_scripts`: LUA tab icon
> * `icon_skins`: SKINS tab icon
> * `icon_cloud`: cloud icon
> * `icon_file`: file icon
> * `icon_refresh`: refresh icon
> * `icon_save`: save icon
> * `icon_configs`: "Configs" popup icon
> * `icon_keys`: keyboard icon
> * `icon_info`: "About" popup icon
> * `icon_close`: close icon (cross)
> * `icon_load`: load icon
> * `icon_import`: import icon
> * `icon_export`: export icon
> * `icon_delete`: delete icon
> * `icon_autoload`: "Autoload" icon
> * `icon_allow_insecure`: "Allow insecure" icon
> * `icon_cloud_upd`: cloud update icon
> * `player_texture`: player preview texture

### fonts﻿ <a href="#fonts" id="fonts"></a>

FieldRead Only

Type: [`accessor<font_base>`](https://lua.fatality.win/accessor.html)

A string to [`font_base`](https://lua.fatality.win/font-base.html) map of all managed fonts. You can query and push fonts with custom IDs. When you add a font to this map, it will be automatically destroyed and recreated when required (such as when DX11 device gets lost).

> ####
>
> Built-in fonts:
>
> * `gui_debug`: Verdana, 13px
> * `gui_title`: Figtree ExtraBold, 23px
> * `gui_main`: Figtree Medium, 14px
> * `gui_main_shadow`: Figree Medium, 14px, with shadow
> * `gui_main_fb`: Segoe UI Semibold, 14px
> * `gui_bold`: Figtree ExtraBold, 14px
> * `gui_bold_fb`: Segoe UI Black, 14px
> * `gui_semi_bold`: Figtree SemiBold, 14px
> * `gui_semi_bold_fb`: Segoe UI Bold, 14px

### shaders﻿ <a href="#shaders" id="shaders"></a>

FieldRead Only

Type: [`accessor<shader>`](https://lua.fatality.win/accessor.html)

A string to [`shader`](https://lua.fatality.win/shader.html) map of all managed shader. You can query and push shader with custom IDs. When you add a shader to this map, it will be automatically destroyed and recreated when required (such as when DX11 device gets lost).

> ####
>
> Build-in shaders:
>
> * `blur_f`: gaussian blur shader

### surface﻿ <a href="#surface" id="surface"></a>

FieldRead Only

Type: [`layer`](https://lua.fatality.win/layer.html)

The layer you can render on.
