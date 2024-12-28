# events

Usage:

`events.{event_name}`

There are a number of events that Fatality provides to use in the API - from various hooks, to in-game events. Each event entry is an object of [`event_t`](https://lua.fatality.win/event-t.html). This table documents events to be used by your scripts.

> ####
>
> You are not required to remove events when your script unloads. It is done automatically by the API engine.

### present\_queue﻿ <a href="#present-queue" id="present-queue"></a>

Field

Invoked each time the game queues a frame for rendering. This is the only permitted location for drawing on screen.

Arguments

None.

### frame\_stage\_notify﻿ <a href="#frame-stage-notify" id="frame-stage-notify"></a>

Field

Invoked every time the game progresses onto another frame stage. This event is called before the game handles a new frame stage.

Arguments

| Name    | Type                                                                     | Description          |
| ------- | ------------------------------------------------------------------------ | -------------------- |
| `stage` | [`client_frame_stage`](https://lua.fatality.win/client-frame-stage.html) | Current frame stage. |

### render\_start\_pre﻿ <a href="#render-start-pre" id="render-start-pre"></a>

Field

Invoked every time game starts the scene rendering process. This event is called before the game's function runs.

Arguments

None.

### render\_start\_post﻿ <a href="#render-start-post" id="render-start-post"></a>

Field

Invoked every time game starts scene rendering process. This event is called after the game's function runs.

Arguments

| Name    | Type                                                       | Description             |
| ------- | ---------------------------------------------------------- | ----------------------- |
| `setup` | [`cview_setup`](https://lua.fatality.win/cview-setup.html) | View setup information. |

### setup\_view\_pre﻿ <a href="#setup-view-pre" id="setup-view-pre"></a>

Field

Invoked every time the game sets up the view. This event is called before the game's function runs.

Arguments

None.

### setup\_view\_post﻿ <a href="#setup-view-post" id="setup-view-post"></a>

Field

Invoked every time the game sets up the view information. This event is called after the game's function runs.

> ####
>
> You can retrieve the view information from `game.view_render` service.

Arguments

None.

### override\_view﻿ <a href="#override-view" id="override-view"></a>

Field

Invoked every time the game internally overrides view information. You are free to change whatever you like in the provided view setup.

Arguments

| Name    | Type                                                       | Description             |
| ------- | ---------------------------------------------------------- | ----------------------- |
| `setup` | [`cview_setup`](https://lua.fatality.win/cview-setup.html) | View setup information. |

### event﻿ <a href="#event" id="event"></a>

Field

Invoked every time a game event fires.

> ####
>
> We do not listen to every single event that exists in the game. If you need something that we don't listen to, please use [`mods.events`](https://lua.fatality.win/events-t.html)

Arguments

| Name    | Type                                                         | Description |
| ------- | ------------------------------------------------------------ | ----------- |
| `event` | [`game_event_t`](https://lua.fatality.win/game-event-t.html) | Game event. |

### handle\_input﻿ <a href="#handle-input" id="handle-input"></a>

Field

Invoked every time the game processes mouse/controller input. This is a good place to alter mouse movement, if needed.

Arguments

| Name    | Type                                                                | Description        |
| ------- | ------------------------------------------------------------------- | ------------------ |
| `type`  | [`input_type_t`](https://lua.fatality.win/input-type-t.html)        | Type of the input. |
| `value` | [`ref_holder_t<float>`](https://lua.fatality.win/ref-holder-t.html) | Input value.       |
