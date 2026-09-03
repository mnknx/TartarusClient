# TartarusClient

**A modern DDNet client with a redesigned dark interface and quality-of-life features.**

TartarusClient is a custom [DDraceNetwork](https://ddnet.org) client focused on a clean, modern look and low-latency gameplay. It ships with a fully reskinned "Tartarus" UI, a tunable fast-input engine, and a set of extra HUD tools — while keeping the full feature set of the underlying client intact.

> Built on top of DDNet and TClient. All original engine and gameplay credit goes to those projects (see [Credits](#credits)).

## Features

### Tartarus UI
- Dark, modern theme applied across the whole client (start screen, main menu, in-game menu, settings)
- Redesigned start screen with an **Tartarus** wordmark and a live list of players currently using the client
- Left navigation rail + top bar layout instead of the classic tab bar
- Adjustable interface scale (default **75%**) so everything fits on smaller screens
- Central theme system — one place defines every color, spacing and size token

### Fast Input
- Low-latency prediction that applies new inputs to your local tee immediately
- **5 modes** — Balanced, Classic, Precise, Aggressive, Maximum
- Millisecond-based amount (tune it to your ping), optional "apply to other tees"
- Configured entirely from the **Tartarus** settings tab

### HUD Widgets
Movable, scalable on-screen tools:
- **Key indicator** — live movement / jump / hook / fire state
- **Input visualizer** — aim dial with angle and inputs
- **Session statistics** — playtime, deaths, finishes
- **Team indicator** — frozen teammates and last-one-standing warning
- **Ninja timer** — countdown bar above tees with an active ninja
- **Hitbox** — draws the real 28×28 physics hitbox

### Localization
- Full **Turkish** translation of the interface (Tartarus + inherited features)

## Installation

- Download the latest **[release](../../releases)** (Windows `.zip`) and run `DDNet.exe`
- Or build it yourself (see below)

## Building (Windows)

You need [Visual Studio](https://visualstudio.microsoft.com/) with the C++ toolchain and the DDNet prebuilt libraries (`ddnet-libs`).

For a full from-source setup (dependencies, other platforms) follow the [DDNet build guide](https://github.com/ddnet/ddnet?tab=readme-ov-file#cloning). The build output is `build\DDNet.exe`.

## Configuration

Tartarus settings live in the **Tartarus** tab of the in-game settings menu, or as console variables:

| Variable | Description |
| --- | --- |
| `cl_Tartarus_ui` | Toggle the Tartarus UI theme |
| `cl_Tartarus_ui_scale` | Interface scale in percent (50–200, default 75) |
| `ta_fast_input` / `ta_fast_input_mode` / `ta_fast_input_amount` | Fast input engine |
| `ta_key_indicator`, `ta_input_visualizer`, `ta_session_stats`, `ta_team_indicator`, `ta_ninja_timer`, `ta_show_hitbox` | HUD widgets |

## Credits

TartarusClient stands on the shoulders of:

- **[DDNet](https://github.com/ddnet/ddnet)** — the engine and game
- **[TClient](https://github.com/sjrc6/TaterClient-ddnet)** — the customization base this client extends

Please support the upstream projects.
