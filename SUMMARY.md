# Table of contents

* [Fatality API](README.md)
* [Getting Started](getting-started/README.md)
  * [First Steps](getting-started/first-steps.md)
  * [Adding UI](getting-started/adding-ui.md)
  * [Creating Libraries](getting-started/creating-libraries.md)
* [API Reference](api-reference/README.md)
  * [Global Functions](api-reference/global-functions.md)
  * [Common Types](api-reference/common-types/README.md)
    * [ptr](api-reference/common-types/ptr.md)
    * [vector](api-reference/common-types/vector.md)
    * [color](api-reference/common-types/color.md)
    * [cview\_setup](api-reference/common-types/cview_setup.md)
    * [game\_event\_t](api-reference/common-types/game_event_t.md)
    * [ref\_holder\_t](api-reference/common-types/ref_holder_t.md)
  * [Common Enums](api-reference/common-enums/README.md)
    * [client\_frame\_stage](api-reference/common-enums/client_frame_stage.md)
    * [input\_type\_t](api-reference/common-enums/input_type_t.md)
  * [math](api-reference/math.md)
  * [events](api-reference/events/README.md)
    * [event\_t](api-reference/events/event_t.md)
  * [game](api-reference/game/README.md)
    * [global\_vars\_t](api-reference/game/global_vars_t.md)
    * [cengine\_client](api-reference/game/cengine_client/README.md)
      * [cnet\_chan](api-reference/game/cengine_client/cnet_chan.md)
  * [mods](api-reference/mods/README.md)
    * [events\_t](api-reference/mods/events_t.md)
  * [entities](api-reference/entities/README.md)
    * [entity\_list\_t](api-reference/entities/entity_list_t/README.md)
      * [entity\_entry\_t](api-reference/entities/entity_list_t/entity_entry_t.md)
    * [base\_entity](api-reference/entities/base_entity/README.md)
      * [schema\_accessor\_t](api-reference/entities/base_entity/schema_accessor_t.md)
      * [cs2\_weapon\_base\_gun](api-reference/entities/base_entity/cs2_weapon_base_gun.md)
      * [cs2\_player\_pawn](api-reference/entities/base_entity/cs2_player_pawn.md)
      * [cs2\_player\_controller](api-reference/entities/base_entity/cs2_player_controller.md)
      * [cs2\_weapon\_base](api-reference/entities/base_entity/cs2_weapon_base.md)
      * [cs2\_grenade\_projectile](api-reference/entities/base_entity/cs2_grenade_projectile.md)
    * [ccsweapon\_base\_vdata](api-reference/entities/ccsweapon_base_vdata/README.md)
      * [cfiring\_mode](api-reference/entities/ccsweapon_base_vdata/cfiring_mode.md)
    * [chandle](api-reference/entities/chandle.md)
    * [csweapon\_mode](api-reference/entities/csweapon_mode.md)
    * [csweapon\_type](api-reference/entities/csweapon_type.md)
    * [weapon\_id](api-reference/entities/weapon_id.md)
    * [csweapon\_category](api-reference/entities/csweapon_category.md)
    * [observer\_mode\_t](api-reference/entities/observer_mode_t.md)
  * [draw](api-reference/draw/README.md)
    * [Common Types](api-reference/draw/common-types/README.md)
      * [rect](api-reference/draw/common-types/rect.md)
      * [vec2](api-reference/draw/common-types/vec2.md)
      * [color](api-reference/draw/common-types/color.md)
      * [accessor](api-reference/draw/common-types/accessor.md)
    * [adapter](api-reference/draw/adapter.md)
    * [layer](api-reference/draw/layer/README.md)
      * [outline\_mode](api-reference/draw/layer/outline_mode.md)
      * [rounding](api-reference/draw/layer/rounding.md)
      * [glow\_parts](api-reference/draw/layer/glow_parts.md)
      * [text\_params](api-reference/draw/layer/text_params/README.md)
        * [text\_alignment](api-reference/draw/layer/text_params/text_alignment.md)
      * [shadow\_dir](api-reference/draw/layer/shadow_dir.md)
      * [command](api-reference/draw/layer/command/README.md)
        * [Page 1](api-reference/draw/layer/command/page-1.md)
    * [managed](api-reference/draw/managed/README.md)
      * [texture](api-reference/draw/managed/texture/README.md)
        * [svg\_texture](api-reference/draw/managed/texture/svg_texture.md)
        * [animated\_texture](api-reference/draw/managed/texture/animated_texture.md)
      * [shader](api-reference/draw/managed/shader.md)
      * [font\_base](api-reference/draw/managed/font_base/README.md)
        * [font](api-reference/draw/managed/font_base/font.md)
        * [font\_gdi](api-reference/draw/managed/font_base/font_gdi.md)
        * [glyph\_t](api-reference/draw/managed/font_base/glyph_t.md)
        * [font\_flags](api-reference/draw/managed/font_base/font_flags.md)
  * [gui](api-reference/gui/README.md)
    * [Common Types](api-reference/gui/common-types/README.md)
      * [bits](api-reference/gui/common-types/bits.md)
      * [control\_id](api-reference/gui/common-types/control_id.md)
    * [context](api-reference/gui/context/README.md)
      * [user\_t](api-reference/gui/context/user_t.md)
    * [notification\_system](api-reference/gui/notification_system/README.md)
      * [notification](api-reference/gui/notification_system/notification.md)
    * [control](api-reference/gui/control/README.md)
      * [control\_type](api-reference/gui/control/control_type.md)
      * [value\_param](api-reference/gui/control/value_param.md)
      * [checkbox](api-reference/gui/control/checkbox.md)
    * [container](api-reference/gui/container/README.md)
      * [control\_container](api-reference/gui/container/control_container/README.md)
        * [layout](api-reference/gui/container/control_container/layout.md)
        * [group](api-reference/gui/container/control_container/group.md)
