# ccsweapon\_base\_vdata

This type represents a weapon's static data.

### built\_right\_handed﻿ <a href="#built-right-handed" id="built-right-handed"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon is designed for right-handed use.

### allow\_flipping﻿ <a href="#allow-flipping" id="allow-flipping"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon can be flipped for left-handed use.

### linked\_cooldowns﻿ <a href="#linked-cooldowns" id="linked-cooldowns"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon's cooldowns are linked with other weapons.

### flags﻿ <a href="#flags" id="flags"></a>

FieldRead Only

Type: `int`

Represents various flags associated with the weapon.

### primary\_ammo\_type﻿ <a href="#primary-ammo-type" id="primary-ammo-type"></a>

FieldRead Only

Type: `int`

The type of ammo used in the primary clip.

### secondary\_ammo\_type﻿ <a href="#secondary-ammo-type" id="secondary-ammo-type"></a>

FieldRead Only

Type: `int`

The type of ammo used in the secondary clip.

### max\_clip1﻿ <a href="#max-clip1" id="max-clip1"></a>

FieldRead Only

Type: `int`

The maximum number of rounds the primary clip can hold.

### max\_clip2﻿ <a href="#max-clip2" id="max-clip2"></a>

FieldRead Only

Type: `int`

The maximum number of rounds the secondary clip can hold.

### default\_clip1﻿ <a href="#default-clip1" id="default-clip1"></a>

FieldRead Only

Type: `int`

The default number of rounds in the primary clip.

### default\_clip2﻿ <a href="#default-clip2" id="default-clip2"></a>

FieldRead Only

Type: `int`

The default number of rounds in the secondary clip.

### reserve\_ammo\_as\_clips﻿ <a href="#reserve-ammo-as-clips" id="reserve-ammo-as-clips"></a>

FieldRead Only

Type: `bool`

Indicates whether reserve ammo is stored as additional clips.

### weight﻿ <a href="#weight" id="weight"></a>

FieldRead Only

Type: `int`

Represents the weight of the weapon.

### auto\_switch\_to﻿ <a href="#auto-switch-to" id="auto-switch-to"></a>

FieldRead Only

Type: `bool`

Indicates whether the game will automatically switch to this weapon when picked up.

### auto\_switch\_from﻿ <a href="#auto-switch-from" id="auto-switch-from"></a>

FieldRead Only

Type: `bool`

Indicates whether the game will automatically switch away from this weapon.

### rumble\_effect﻿ <a href="#rumble-effect" id="rumble-effect"></a>

FieldRead Only

Type: `int`

Represents the rumble effect associated with this weapon.

### slot﻿ <a href="#slot" id="slot"></a>

FieldRead Only

Type: `int`

The inventory slot this weapon occupies.

### position﻿ <a href="#position" id="position"></a>

FieldRead Only

Type: `int`

The position of the weapon in the inventory slot.

### weapon\_type﻿ <a href="#weapon-type" id="weapon-type"></a>

FieldRead Only

Type: [`csweapon_type`](https://lua.fatality.win/csweapon-type.html)

The type of the weapon.

### weapon\_category﻿ <a href="#weapon-category" id="weapon-category"></a>

FieldRead Only

Type: [`csweapon_category`](https://lua.fatality.win/csweapon-category.html)

The category of the weapon.

### gear\_slot﻿ <a href="#gear-slot" id="gear-slot"></a>

FieldRead Only

Type: `int`

Represents the gear slot associated with the weapon.

### gear\_slot\_position﻿ <a href="#gear-slot-position" id="gear-slot-position"></a>

FieldRead Only

Type: `int`

The position of the weapon in the gear slot.

### default\_loadout\_slot﻿ <a href="#default-loadout-slot" id="default-loadout-slot"></a>

FieldRead Only

Type: `int`

The default loadout slot for the weapon.

### s\_wrong\_team\_msg﻿ <a href="#s-wrong-team-msg" id="s-wrong-team-msg"></a>

FieldRead Only

Type: `string`

The message displayed when the weapon is used by the wrong team.

### price﻿ <a href="#price" id="price"></a>

FieldRead Only

Type: `int`

The purchase price of the weapon.

### kill\_award﻿ <a href="#kill-award" id="kill-award"></a>

FieldRead Only

Type: `int`

The cash reward given to the player for a kill with this weapon.

### primary\_reserve\_ammo\_max﻿ <a href="#primary-reserve-ammo-max" id="primary-reserve-ammo-max"></a>

FieldRead Only

Type: `int`

The maximum amount of reserve ammo for the primary clip.

### secondary\_reserve\_ammo\_max﻿ <a href="#secondary-reserve-ammo-max" id="secondary-reserve-ammo-max"></a>

FieldRead Only

Type: `int`

The maximum amount of reserve ammo for the secondary clip.

### melee\_weapon﻿ <a href="#melee-weapon" id="melee-weapon"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon is classified as a melee weapon.

### has\_burst\_mode﻿ <a href="#has-burst-mode" id="has-burst-mode"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon has a burst fire mode.

### is\_revolver﻿ <a href="#is-revolver" id="is-revolver"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon is classified as a revolver.

### cannot\_shoot\_underwater﻿ <a href="#cannot-shoot-underwater" id="cannot-shoot-underwater"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon cannot be fired underwater.

### name﻿ <a href="#name" id="name"></a>

FieldRead Only

Type: `string`

The internal name of the weapon.

### anim\_extension﻿ <a href="#anim-extension" id="anim-extension"></a>

FieldRead Only

Type: `string`

The animation extension used by the weapon.

### e\_silencer\_type﻿ <a href="#e-silencer-type" id="e-silencer-type"></a>

FieldRead Only

Type: `int`

Represents the type of silencer compatible with the weapon.

### crosshair\_min\_distance﻿ <a href="#crosshair-min-distance" id="crosshair-min-distance"></a>

FieldRead Only

Type: `int`

The minimum crosshair spread distance for this weapon.

### crosshair\_delta\_distance﻿ <a href="#crosshair-delta-distance" id="crosshair-delta-distance"></a>

FieldRead Only

Type: `int`

The change in crosshair spread distance when firing.

### is\_full\_auto﻿ <a href="#is-full-auto" id="is-full-auto"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon is fully automatic.

### num\_bullets﻿ <a href="#num-bullets" id="num-bullets"></a>

FieldRead Only

Type: `int`

The number of bullets fired per shot.

### cycle\_time﻿ <a href="#cycle-time" id="cycle-time"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The time between successive shots.

### max\_speed﻿ <a href="#max-speed" id="max-speed"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The maximum movement speed of the player while holding this weapon.

### spread﻿ <a href="#spread" id="spread"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The base spread of the weapon when fired.

### inaccuracy\_crouch﻿ <a href="#inaccuracy-crouch" id="inaccuracy-crouch"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The inaccuracy of the weapon while crouching.

### inaccuracy\_stand﻿ <a href="#inaccuracy-stand" id="inaccuracy-stand"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The inaccuracy of the weapon while standing.

### inaccuracy\_jump﻿ <a href="#inaccuracy-jump" id="inaccuracy-jump"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The inaccuracy of the weapon while jumping.

### inaccuracy\_land﻿ <a href="#inaccuracy-land" id="inaccuracy-land"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The inaccuracy of the weapon upon landing from a jump.

### inaccuracy\_ladder﻿ <a href="#inaccuracy-ladder" id="inaccuracy-ladder"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The inaccuracy of the weapon while climbing a ladder.

### inaccuracy\_fire﻿ <a href="#inaccuracy-fire" id="inaccuracy-fire"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The inaccuracy of the weapon while firing.

### inaccuracy\_move﻿ <a href="#inaccuracy-move" id="inaccuracy-move"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The inaccuracy of the weapon while moving.

### recoil\_angle﻿ <a href="#recoil-angle" id="recoil-angle"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The angle of recoil for the weapon when fired.

### recoil\_angle\_variance﻿ <a href="#recoil-angle-variance" id="recoil-angle-variance"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The variance in the angle of recoil.

### recoil\_magnitude﻿ <a href="#recoil-magnitude" id="recoil-magnitude"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The magnitude of recoil for the weapon.

### recoil\_magnitude\_variance﻿ <a href="#recoil-magnitude-variance" id="recoil-magnitude-variance"></a>

FieldRead Only

Type: [`cfiring_mode<float>`](https://lua.fatality.win/cfiring-mode.html)

The variance in the magnitude of recoil.

### tracer\_frequency﻿ <a href="#tracer-frequency" id="tracer-frequency"></a>

FieldRead Only

Type: [`cfiring_mode<int>`](https://lua.fatality.win/cfiring-mode.html)

The frequency of tracers visible when firing the weapon.

### inaccuracy\_jump\_initial﻿ <a href="#inaccuracy-jump-initial" id="inaccuracy-jump-initial"></a>

FieldRead Only

Type: `float`

The initial inaccuracy of the weapon upon jumping.

### inaccuracy\_jump\_apex﻿ <a href="#inaccuracy-jump-apex" id="inaccuracy-jump-apex"></a>

FieldRead Only

Type: `float`

The inaccuracy of the weapon at the apex of a jump.

### inaccuracy\_reload﻿ <a href="#inaccuracy-reload" id="inaccuracy-reload"></a>

FieldRead Only

Type: `float`

The inaccuracy of the weapon after reloading.

### recoil\_seed﻿ <a href="#recoil-seed" id="recoil-seed"></a>

FieldRead Only

Type: `int`

The seed value used for determining recoil patterns.

### spread\_seed﻿ <a href="#spread-seed" id="spread-seed"></a>

FieldRead Only

Type: `int`

The seed value used for determining weapon spread.

### time\_to\_idle\_after\_fire﻿ <a href="#time-to-idle-after-fire" id="time-to-idle-after-fire"></a>

FieldRead Only

Type: `float`

The time it takes for the weapon to transition to idle after firing.

### idle\_interval﻿ <a href="#idle-interval" id="idle-interval"></a>

FieldRead Only

Type: `float`

The time interval between idle animations for the weapon.

### attack\_movespeed\_factor﻿ <a href="#attack-movespeed-factor" id="attack-movespeed-factor"></a>

FieldRead Only

Type: `float`

The factor by which the player's movement speed is reduced while attacking with this weapon.

### heat\_per\_shot﻿ <a href="#heat-per-shot" id="heat-per-shot"></a>

FieldRead Only

Type: `float`

The heat generated by the weapon per shot.

### inaccuracy\_pitch\_shift﻿ <a href="#inaccuracy-pitch-shift" id="inaccuracy-pitch-shift"></a>

FieldRead Only

Type: `float`

The pitch shift caused by inaccuracy when firing.

### inaccuracy\_alt\_sound\_threshold﻿ <a href="#inaccuracy-alt-sound-threshold" id="inaccuracy-alt-sound-threshold"></a>

FieldRead Only

Type: `float`

The threshold for inaccuracy at which an alternative sound is played.

### bot\_audible\_range﻿ <a href="#bot-audible-range" id="bot-audible-range"></a>

FieldRead Only

Type: `float`

The range at which bots can hear this weapon being fired.

### use\_radio\_subtitle﻿ <a href="#use-radio-subtitle" id="use-radio-subtitle"></a>

FieldRead Only

Type: `string`

Indicates whether this weapon uses radio subtitles for its actions.

### unzooms\_after\_shot﻿ <a href="#unzooms-after-shot" id="unzooms-after-shot"></a>

FieldRead Only

Type: `bool`

Indicates whether the weapon unzooms automatically after firing.

### hide\_view\_model\_when\_zoomed﻿ <a href="#hide-view-model-when-zoomed" id="hide-view-model-when-zoomed"></a>

FieldRead Only

Type: `bool`

Indicates whether the view model is hidden when the weapon is zoomed in.

### zoom\_levels﻿ <a href="#zoom-levels" id="zoom-levels"></a>

FieldRead Only

Type: `int`

The number of zoom levels available for this weapon.

### zoom\_fov1﻿ <a href="#zoom-fov1" id="zoom-fov1"></a>

FieldRead Only

Type: `int`

The field of view (FOV) for the first zoom level.

### zoom\_fov2﻿ <a href="#zoom-fov2" id="zoom-fov2"></a>

FieldRead Only

Type: `int`

The field of view (FOV) for the second zoom level.

### zoom\_time0﻿ <a href="#zoom-time0" id="zoom-time0"></a>

FieldRead Only

Type: `float`

The time it takes to transition to the initial zoom state.

### zoom\_time1﻿ <a href="#zoom-time1" id="zoom-time1"></a>

FieldRead Only

Type: `float`

The time it takes to transition to the first zoom level.

### zoom\_time2﻿ <a href="#zoom-time2" id="zoom-time2"></a>

FieldRead Only

Type: `float`

The time it takes to transition to the second zoom level.

### iron\_sight\_pull\_up\_speed﻿ <a href="#iron-sight-pull-up-speed" id="iron-sight-pull-up-speed"></a>

FieldRead Only

Type: `float`

The speed at which the weapon's iron sights are pulled up.

### iron\_sight\_put\_down\_speed﻿ <a href="#iron-sight-put-down-speed" id="iron-sight-put-down-speed"></a>

FieldRead Only

Type: `float`

The speed at which the weapon's iron sights are put down.

### iron\_sight\_fov﻿ <a href="#iron-sight-fov" id="iron-sight-fov"></a>

FieldRead Only

Type: `float`

The field of view (FOV) when aiming down the weapon's iron sights.

### iron\_sight\_pivot\_forward﻿ <a href="#iron-sight-pivot-forward" id="iron-sight-pivot-forward"></a>

FieldRead Only

Type: `float`

The forward pivot point for the weapon's iron sights.

### iron\_sight\_looseness﻿ <a href="#iron-sight-looseness" id="iron-sight-looseness"></a>

FieldRead Only

Type: `float`

The looseness of the weapon's iron sights when aiming.

### ang\_pivot\_angle﻿ <a href="#ang-pivot-angle" id="ang-pivot-angle"></a>

FieldRead Only

Type: [`vector`](https://lua.fatality.win/vector.html)

The pivot angle for the weapon's iron sights.

### vec\_iron\_sight\_eye\_pos﻿ <a href="#vec-iron-sight-eye-pos" id="vec-iron-sight-eye-pos"></a>

FieldRead Only

Type: [`vector`](https://lua.fatality.win/vector.html)

The eye position when aiming down the weapon's iron sights.

### damage﻿ <a href="#damage" id="damage"></a>

FieldRead Only

Type: `int`

The base damage dealt by the weapon.

### headshot\_multiplier﻿ <a href="#headshot-multiplier" id="headshot-multiplier"></a>

FieldRead Only

Type: `float`

The multiplier applied to damage for headshots.

### armor\_ratio﻿ <a href="#armor-ratio" id="armor-ratio"></a>

FieldRead Only

Type: `float`

The ratio determining how much damage penetrates armor.

### penetration﻿ <a href="#penetration" id="penetration"></a>

FieldRead Only

Type: `float`

The penetration power of the weapon for materials.

### range﻿ <a href="#range" id="range"></a>

FieldRead Only

Type: `float`

The effective range of the weapon.

### range\_modifier﻿ <a href="#range-modifier" id="range-modifier"></a>

FieldRead Only

Type: `float`

The modifier applied to damage based on range.

### flinch\_velocity\_modifier\_large﻿ <a href="#flinch-velocity-modifier-large" id="flinch-velocity-modifier-large"></a>

FieldRead Only

Type: `float`

The velocity modifier for large flinch effects.

### flinch\_velocity\_modifier\_small﻿ <a href="#flinch-velocity-modifier-small" id="flinch-velocity-modifier-small"></a>

FieldRead Only

Type: `float`

The velocity modifier for small flinch effects.

### recovery\_time\_crouch﻿ <a href="#recovery-time-crouch" id="recovery-time-crouch"></a>

FieldRead Only

Type: `float`

The recovery time for accuracy when crouching.

### recovery\_time\_stand﻿ <a href="#recovery-time-stand" id="recovery-time-stand"></a>

FieldRead Only

Type: `float`

The recovery time for accuracy when standing.

### recovery\_time\_crouch\_final﻿ <a href="#recovery-time-crouch-final" id="recovery-time-crouch-final"></a>

FieldRead Only

Type: `float`

The final recovery time for accuracy when crouching.

### recovery\_time\_stand\_final﻿ <a href="#recovery-time-stand-final" id="recovery-time-stand-final"></a>

FieldRead Only

Type: `float`

The final recovery time for accuracy when standing.

### recovery\_transition\_start\_bullet﻿ <a href="#recovery-transition-start-bullet" id="recovery-transition-start-bullet"></a>

FieldRead Only

Type: `int`

The starting bullet count for recovery transition.

### recovery\_transition\_end\_bullet﻿ <a href="#recovery-transition-end-bullet" id="recovery-transition-end-bullet"></a>

FieldRead Only

Type: `int`

The ending bullet count for recovery transition.

### throw\_velocity﻿ <a href="#throw-velocity" id="throw-velocity"></a>

FieldRead Only

Type: `float`

The velocity of thrown items (e.g., grenades).

### v\_smoke\_color﻿ <a href="#v-smoke-color" id="v-smoke-color"></a>

FieldRead Only

Type: [`vector`](https://lua.fatality.win/vector.html)

The color of smoke effects for this weapon.

### anim\_class﻿ <a href="#anim-class" id="anim-class"></a>

FieldRead Only

Type: `string`

The animation class associated with this weapon.
