# ElysiumClient

**A modern DDNet client with a redesigned dark interface and quality-of-life features.**

ElysiumClient is a custom [DDraceNetwork](https://ddnet.org) client focused on a clean, modern look and low-latency gameplay. It ships with a fully reskinned "Elysium" UI, a tunable fast-input engine, and a set of extra HUD tools — while keeping the full feature set of the underlying client intact.

> Built on top of DDNet and TClient. All original engine and gameplay credit goes to those projects (see [Credits](#credits)).

## Features

### Elysium UI
- Dark, modern theme applied across the whole client (start screen, main menu, in-game menu, settings)
- Redesigned start screen with an **ELYSIUM** wordmark and a live list of players currently using the client
- Left navigation rail + top bar layout instead of the classic tab bar
- Adjustable interface scale (default **75%**) so everything fits on smaller screens
- Central theme system — one place defines every color, spacing and size token

### Fast Input
- Low-latency prediction that applies new inputs to your local tee immediately
- **5 modes** — Balanced, Classic, Precise, Aggressive, Maximum
- Millisecond-based amount (tune it to your ping), optional "apply to other tees"
- Configured entirely from the **Elysium** settings tab

### HUD Widgets
Movable, scalable on-screen tools:
- **Key indicator** — live movement / jump / hook / fire state
- **Input visualizer** — aim dial with angle and inputs
- **Session statistics** — playtime, deaths, finishes
- **Team indicator** — frozen teammates and last-one-standing warning
- **Ninja timer** — countdown bar above tees with an active ninja
- **Hitbox** — draws the real 28×28 physics hitbox

### Localization
- Full **Turkish** translation of the interface (Elysium + inherited features)

## Installation

- Download the latest **[release](../../releases)** (Windows `.zip`) and run `DDNet.exe`
- Or build it yourself (see below)

## Building (Windows)

You need [Visual Studio](https://visualstudio.microsoft.com/) with the C++ toolchain and the DDNet prebuilt libraries (`ddnet-libs`).

For a full from-source setup (dependencies, other platforms) follow the [DDNet build guide](https://github.com/ddnet/ddnet?tab=readme-ov-file#cloning). The build output is `build\DDNet.exe`.

## Configuration

Elysium settings live in the **Elysium** tab of the in-game settings menu, or as console variables:

| Variable | Description |
| --- | --- |
| `cl_elysium_ui` | Toggle the Elysium UI theme |
| `cl_elysium_ui_scale` | Interface scale in percent (50–200, default 75) |
| `el_fast_input` / `el_fast_input_mode` / `el_fast_input_amount` | Fast input engine |
| `el_key_indicator`, `el_input_visualizer`, `el_session_stats`, `el_team_indicator`, `el_ninja_timer`, `el_show_hitbox` | HUD widgets |

## Credits

ElysiumClient stands on the shoulders of:

- **[DDNet](https://github.com/ddnet/ddnet)** — the engine and game
- **[TClient](https://github.com/sjrc6/TaterClient-ddnet)** — the customization base this client extends

Please support the upstream projects.
