<div align="center">

<img src="https://cdn.discordapp.com/attachments/941510112328159305/1510788495428550856/AviationSystems.png?ex=6a1e16ee&is=6a1cc56e&hm=462dcaa12c5d6c31358603950e19f9038d5604c4047e44e4b0f0f5bf10d44fd3&" alt="Aircraft Systems" width="600">

# Aircraft Systems

[![Discord](https://img.shields.io/discord/1363054298736492694?label=Discord&logo=discord&logoColor=white&color=5865F2)](https://discord.gg/YhQgs2ucGY)
[![License](https://img.shields.io/badge/License-APL-blue)](https://github.com/10thrangerregiment-dev/Aircraft-Systems?tab=License-1-ov-file)
[![Credits](https://img.shields.io/badge/Credits-View-green)](https://github.com/10thrangerregiment-dev/Aircraft-Systems/blob/main/credits)

*Bridging the gap between Arma 3 and Arma Reforger aviation.*

</div>

---

## About

The **10th Ranger Regiment** is happy to present **Aircraft Systems** - a mod that brings the data systems, situational awareness, and quality-of-life features Arma 3 pilots took for granted into Arma Reforger.

Everything's packaged to work together out of the box, but the features are loosely coupled, developers can unlink whichever pieces they don't want for their own airframes.

---

##  Features

###  Targeting Pod (TGP)

A pilot-accessible, full-screen stabilized camera that keeps you in full control of the aircraft and its weapons.

- **Information suite** — aircraft and reticle position data, target store with quick-slew and reference
- **Day / IR / Thermal** *(full capability requires dependencies)*
- **6 zoom steps** — stepped, smooth, or hybrid
- **Slew to grid** or **slew to map click**
- **Area + point geolock** — pin the camera to a spot and fly around it
- **HADS marker placement** with a toggleable in-view overlay; synced across maps and other pilots' overlays in multiplayer
- **IR Sparkle** — Air-to-Ground Laser
- **Target storage** — store three targets, slew back to them, reference them from the HMD
- **Terrain avoidance** — predictive terrain collision warning
- **Configurable settings** 

###  Helmet-Mounted Display (HMD)

Out-the-window symbology layered over your forward view.

- **Information suite** — pitch/roll horizon, speed, altitude, heading, vertical speed, fuel, TGP aimpoint indicator, autohover indicator
- **Weapons suite** — current weapon indicator, dumb-fire rocket and gun CCIP
- **Flight computer** — visual indicators with time-of-flight information
  - **RTE system** — auto-builds a flight route from map markers
  - **WP system** — single waypoint by grid or map pick
  - **TGT system** — pulls from your TGP's stored targets

---

## 📦 Installation

Aircraft Systems comes **pre-packaged on specific airframes**. Subscribe to the airframe mod on the Workshop and the appropriate Aircraft Systems variant comes with it — no separate install needed.

If you're a mod developer integrating Aircraft Systems into your own aircraft, see the variants below to pick which one matches your needs.

### Variants

| Variant | Dependencies | Features |
|---|---|---|
| **Aircraft Systems — Core** | None | Full TGP and HMD functionality **except** IR Sparkle and Thermal | Green Beam Sparkle
| **Aircraft Systems — RHS Compat** | RHS: Status Quo, Thermal Post Process | Everything, including IR Sparkle and Thermal |
| **Aircraft Systems — NVS Compat** | Night Vision System, Thermal Post Process Assets | Everything, including IR Sparkle and Thermal | 
> [!NOTE]
> Pick **Core** if you want a lightweight install with no third-party mod dependencies. Pick **Utility** if you want the full feature set — thermal optics and a working IR sparkle for night ops.

### Support Aircraft


> [!NOTE]
> Due to 1.7, this is pretty bare. As things come back online, there will be more. 
---

## 📡 Operator's Guide

> A pilot's walkthrough of the Targeting Pod and Helmet-Mounted Display. Read it once, fly with it open the second time.

> [!IMPORTANT]
> **It is HIGHLY recomended that everything is rebound. Most choices were made for debugging, through use a 12 button MMO mouse.

### 📋 Table of Contents

- [Part 1 — The Targeting Pod (TGP)](#part-1--the-targeting-pod-tgp)
  - [What it is](#what-it-is)
  - [Looking around](#looking-around)
  - [Zoom — two modes in one](#zoom--two-modes-in-one)
  - [Slewing to a grid](#slewing-to-a-grid)
  - [Slewing to a map click](#slewing-to-a-map-click)
  - [Geolock — pin the camera to a spot](#geolock--pin-the-camera-to-a-spot)
  - [Auto-lock — set and forget](#auto-lock--set-and-forget)
  - [Target slots — three points of memory](#target-slots--three-points-of-memory)
  - [Dropping map markers](#dropping-map-markers)
  - [Thermal — `Shift+N`](#thermal--shiftn)
  - [Sparkle — `Shift+J`](#sparkle--shiftj)
  - [BFT — `Shift+B`](#bft--shiftb)
  - [Terrain warning](#terrain-warning)
  - [Settings — `Shift+P`](#settings--shiftp)
- [Part 2 — The Helmet-Mounted Display (HMD)](#part-2--the-helmet-mounted-display-hmd)
  - [What it is](#what-it-is-1)
  - [What you see](#what-you-see)
  - [CCIP — where your rounds will land](#ccip--where-your-rounds-will-land)
  - [Waypoint indicator — three modes](#waypoint-indicator--three-modes)
    - [Mode 1 — `WP` (single waypoint, yours)](#mode-1--wp-single-waypoint-yours)
    - [Mode 2 — `RTE` (route, auto-discovered)](#mode-2--rte-route-auto-discovered)
    - [Mode 3 — `TGT` (TGP's selected target slot)](#mode-3--tgt-tgps-selected-target-slot)
  - [TGP aim icon — the small floating dot](#tgp-aim-icon--the-small-floating-dot)
  - [Slew TGP to waypoint — `NumPad 6`](#slew-tgp-to-waypoint--numpad-6)
- [Part 3 — How the two systems work together](#part-3--how-the-two-systems-work-together)
- [⌨️ Quick keybind chart](#️-quick-keybind-chart)
- [🛠️ Troubleshooting](#️-troubleshooting)

---

### Part 1 — The Targeting Pod (TGP)

#### What it is

Sit in the pilot seat and press **`T`**. The screen swaps from your normal pilot view to a stabilized camera looking out from the aircraft's gimbal. This pod comes with many features to aid in ISR/SA.

Press **`T`** again to come back to the cockpit.

> [!IMPORTANT]
> **You can't disembark while the TGP is open.** Press `T` to close it, then step out. This is intentional.

#### Looking around

Mouse moves the camera. So does your head — turn it, and the gimbal follows. The screen-center reticle is where the trace lands; that's your "aim point" for almost everything else in the pod.
> [!IMPORTANT]
> **If you fly with mouse input enabled, you must hit ALT and then move mouse.** 

What you'll see on the TGP HUD:

- **Camera Zoom** in the top left corner — `CCD` for daylight, `FLIR` when thermal is on
- **Craft Information** (MGRS grid), altitude, airspeed, autohover
- **Directional References** On the left side of the screen, you will see a NORTH arrow. This points to NORTH from your point of aim. Underneath that is the camera position. The 12 o'clock of the circle is the front of the aircraft.
- **Target coordinates** (MGRS grid), elevation, and distance under the reticle
- **Three target slot panels** (more on those shortly)
- **Geolock label** when you have a fixed lock
- **Sparkle Indicator** Indicates that your sparkle is armed

#### Zoom — two modes in one

The TGP has six FOV stops, widest to narrowest. How they behave depends on the **step/smooth threshold** in your settings:

| Mode | Behavior |
|---|---|
| **All step** *(default)* | Every press of `NumPad 5` zooms in one notch. `NumPad 4` zooms out. |
| **All smooth** | Hold `NumPad 5` and the FOV narrows continuously, proportionally — consistent zoom rate whether you're wide or tight. |
| **Hybrid** | Stepped at wide FOVs (where stepping feels natural), smooth at narrow FOVs (where you want fine control on long-range targets). |

You can also flip on **dynamic smoothing** — when you're zoomed in tight, smooth zoom slows down automatically so you don't over-shoot.

> [!TIP]
> Camera wandered into orbit? Hit **`-`** (numpad minus). It snaps the camera forward and slightly down — same orientation it has when you first open the pod.

#### Slewing to a grid

You know the coordinates, you want the camera there. **`G`** opens a small dialog. Type a 6-digit grid (100 m precision) or 8-digit (10 m precision), hit Enter, and the camera slews to that spot.

#### Slewing to a map click

**`Shift+M`** opens the in-game map. Pan and zoom like normal. When the cursor's where you want to look, press **`NumPad 1`** to commit. The camera slews there.

Pressing `Shift+M` while the map's already open closes it. If you accidentally Esc-closed the map without confirming, the next `Shift+M` press picks itself back up cleanly — no need to re-toggle anything.

#### AREA LOCK / GEOLOCK — pin the camera to a spot

Put the reticle on a point in the world and press **`Shift+L`**. The TGP locks onto that position. From now on, no matter how the helicopter maneuvers, the camera stays pointed at that exact spot. You can fly circles around it while the camera tracks.

Press `Shift+L` again to release. The lock breaks in place.

#### POINT LOCK — Automatic, tracking lock

Orient the reticle onto a vehicle or person, hold it for half a second, and the camera will lock. You know it has locked when the "POINT" display pops up in your lock indicator area. 
> [!TIP]
> The best practice is to aim center mass. If you know that you are aiming properly, move the camera around a bit to attempt to get a lock. Laterally moving targets are by far the hardest to lock. 

> [!NOTE]
> Geolock and auto-lock can't both be on — picking one releases the other.


#### Target slots — three points of memory

You can save up to **three target positions** during a sortie.

- **`Shift+S`** — store wherever the reticle's pointing into the next free slot. If all three are full, it rolls over and overwrites the oldest.
- **`NumPad 4`** — cycle which slot is "selected" (the HUD highlights it).
- **`Shift+Tab`** — slew the camera to the selected slot.

In the current state, there is no preprogramming of these. In the future, that will change. 

> [!NOTE]
> These interface with the TGT Waypoint Mode on the HMD. The currently selected display will present an on-screen pip, as well as routing information. 

#### Dropping map markers

**`Y`** drops a marker where the reticle's pointing. The marker shows up on everyone's map. Each marker gets an auto-numbered label using your two-letter prefix: `HM01`, `HM02`, and so on.

**`Shift+Y`** toggles an overlay that draws the labels on the TGP camera view, projected to where each marker is in 3D space. Useful for keeping track of designated points while you're scanning around. You are able to see other aviator's markers with this overlay. 

You can change your two-letter prefix in the settings dialog (default is `HM`).


#### Thermal — `Shift+N`

Toggles FLIR on the camera. 

**`PageUp`** and **`PageDown`** step the gain manually. The TGP also runs an auto-gain mode that tracks scene radiance — gain hands off cleanly between manual and auto.

#### Sparkle — `Shift+J`

An IZLID strapped to a helicopter. When you point the TGP at a target and toggle sparkle on, the aircraft emits an IR visible beam from a point just below the gimbal. 

The beam tracks wherever the reticle is — slew the camera, the beam follows. Sparkle stays armed when you close the TGP, so you can mark a target then close the pod and fly.

> [!NOTE]
> Sparkle remains in place during AREA and POINT lock. So you can lock a target or location, sparkle it, come out of the TGP and meneuver and maintain that sparkle. 

#### Link 16 / Blue Force Tracking — `Shift+B`

Toggles a **Blue Force Tracking** overlay. Friendly group leaders display a real-time tracking icon overtop of them. When a friendly's in a vehicle, the icon attaches to the vehicle, not the body inside. 

Range is 5km per default. 

#### Terrain warning

The TGP looks ahead from the front of the helicopter for obstacles. If the helicopter is projected to impact an object within 8 seconds of flight, it will alert you with an audio/visual indicator. You can configure it three ways in settings: full on (visual + audio), sound off (visual only), or fully off.



#### Settings — `Shift+P`

Opens a dialog (only works when the TGP is up) with:

- **Marker prefix** — change `HM` to whatever two letters you like (We use aviator First/Last initial to differentiate)
- **Step/smooth threshold** — five preset buttons (all step / 45 / 30 / 15 / all smooth). This dictates where step->smoothing transition happens. If you want to step through the far out zooms, and have smoothing in from there, pick a lower option.
- **Smooth zoom rate** — how fast smooth zoom proceeds
- **Dynamic smoothing** — on/off plus a strength slider
- **Terrain avoidance mode** — on / sound-off / off

All these save to a per-pilot file under your profile. They stick across sessions, and can be reset by clicking Cancel + closing without saving. They also save between airframes.

---

### Part 2 —  Helmet-Mounted Display (HMD)

#### What it is

Aviation Display. Press **`Shift+H`** while you're in the pilot seat and a HUD overlay paints itself over your normal forward view. Think of it as the symbology you'd see on a real HMD — heading, attitude, altitude, airspeed, fuel, weapon info, and a few worldspace symbols to assist with situational awareness.

The HMD **hides automatically when the TGP is open** and **comes back automatically when the TGP closes** — if you'd toggled it on. 

#### What you see

**Top of the view** — a compass scroller. Above it you read `HDG 273` (current aircraft heading); separately, `EYE 281` shows where your head is pointing (aircraft heading + neck twist).

**Pitch/Roll Ladder** — A vertical pitch/roll ladder is across the middle. This goes to a maximum of 60 degrees of pitch, and 90 degrees of roll. The center lines up with the right side caret for 0 pitch/roll. 

**VSI** — Vertical Speed Indicator. Caret rides up or down off a fixed zero baseline as your climb/sink rate changes. Below a configurable sink threshold (default −5 m/s), the caret tints **red**.

**Airspeed readout** — To the left of the Pitch/Roll. Displays speed in knots.

**Fuel time** — text label showing time-to-empty at current burn rate. Reads `FUEL 14:32` normally; when remaining time drops below 10 minutes, it switches to `BINGO 04:58`. 

**Weapon name + ammo** — current weapon and the round count. Shows `NO WEP` if the aircraft doesn't have a pilot-controlled weapon.

#### CCIP — Continuously Computed Impact Point 

When the aircraft has a weapon and the HMD's up, the **CCIP pipper** floats in the forward view at the spot where the rounds (or rockets) are predicted to impact — accounting for gravity, drag, your aircraft's motion, and the weapon's actual ballistics.

There are two shapes:

- **Rocket I-beam** — appears when you're armed with Hydra-70 / LAU / S5 / S8. 
- **Gun/cannon crosshair** — appears when you're on M134 / GAU-17 / GAU-19 / GAU-21 / M230 / M242 / chain gun. 

Only one pipper shows at a time. When you cycle weapons, the old pipper hides immediately.

> [!WARNING]
> If the pipper would land beyond engagement range (3 km default), or behind the camera, it hides. 

#### Flight Computer

A visual indicator that points at a "current waypoint" plus a label with the heading, distance, and time-of-flight at current speed. **`Shift+O`** cycles the source of that waypoint.

##### Mode 1 — `WP` (single waypoint, yours)

You set one waypoint, the chevron points at it. Two ways to set:

- **`NumPad 7`** opens a grid dialog. Type 6 or 8 digits, hit Enter, done.
- **`NumPad 8`** opens the map. Click where you want. **`NumPad 9`** confirms.

Only your HMD sees this.

##### Mode 2 — `TGT` (TGP's selected target slot)

The chevron points at whichever target slot you currently have selected in the TGP. Useful for cueing weapons or maintaining situational awareness on a stored target while flying head-out.

Each mode has its own empty-state message (`NO WAYPOINT SET` / `NO ROUTE DATA` / `NO TARGET DATA`).

# Mode 3 - 'RTE' (Route Flight Computer)
 
The Helmet-Mounted Display (HMD) reads route markers placed on the map, links them into an ordered flight route, and guides the aircraft along it. The directional chevron always points toward the next leg, and the route **auto-advances** as each waypoint is reached.
 
## How It Works
 
1. Place the supported markers on the map.
2. The HMD reads them and assembles a route, using the `AFR` marker to name the route and tie the markers together.
3. In flight, the chevron points at the next leg.
4. As you pass each waypoint, the route advances automatically to the next step.
## Marker Reference
 
| Marker   | Name                              | Role                                                                 |
|----------|-----------------------------------|----------------------------------------------------------------------|
| `AFR`    | Army Flight Route                 | Defines the route name and links all markers into one route.         |
| `CP`     | Control Point / Start Point       | The first step (waypoint) of the route.                              |
| `ACP`    | Air Control Point (checkpoint)    | Intermediate checkpoints along the route, sequentially enumerated.   |
| `BP/HA`  | Battle Position / Holding Area    | Staging/holding waypoint along the route.                            |
| `RP`     | Release Point                     | Where aircraft leave the route and proceed to the final destination. |
| `HLZ`    | Helicopter Landing Zone           | Defines the landing zone; the landing point itself when no chalks exist. |
| `C`      | Chalk                             | Links to an `HLZ` to define an individual landing area per chalk.    |
 
## Route Construction
 
The route is built in the following order:
 
- **`AFR`** — Names the route and links the markers together. Required.
- **`CP`** — The starting waypoint, evaluated as the first step.
- **`ACP`** — Additional checkpoints between the start and the release point. Numbered in sequence (`ACP 1`, `ACP 2`, …) and followed in order.
- **`BP/HA`** — A holding or staging waypoint along the route.
- **`RP`** — Marks where the aircraft leaves the route. After the `RP`, the next step is the destination.
- **`HLZ`** — The destination zone. When no chalks are defined, the `HLZ` marker is the landing point.
- **`C`** — Chalks link to an `HLZ` and assign each chalk its own landing area within that zone.
## Minimum Requirements
 
A valid route requires at minimum:
 
- An **`AFR`** marker (to name and link the route), and
- An **endpoint** (an `HLZ`, or another marker that serves as the final destination)


- **`Shift+X`** — cycle destination type (RP / BP / HA / HLZ / Chalk)
- **`Shift+C`** — cycle chalks at the selected LZ
- **`Shift+N`** — force advance to next leg if the automatic capture doesn't trigger (you flew around the CP instead of through it, for instance)

The route is **shared via map markers** — anyone with the right markers placed and the same faction sees the same route on their HMD. 

Each mode has its own empty-state message (`NO WAYPOINT SET` / `NO ROUTE DATA` / `NO TARGET DATA`).


#### TGP aim icon — the small floating dot

Shows the current position of the TGP through your HMD.

#### Slew TGP to waypoint — `NumPad 6`

Press it and the TGP slews to whatever the HMD's current waypoint is. Works in any mode (WP / RTE / TGT). Useful for "I want the TGP looking at the next checkpoint" without typing a grid.

---

### Part 3 — How the two systems work together

A few things cross over between the TGP and the HMD:


- **Target slots** — the HMD's TGT-mode waypoint reads from the TGP's selected target slot. Store a target in the TGP, switch HMD to TGT mode, and you have a chevron pointing at it.
- **TGP aim point** — the HMD draws a small icon at the TGP's current world aim. Lets you fly head-up and still know where the pod is looking.
- **TGP-active hides HMD** — the HMD overlay despawns when the TGP camera comes up, so your forward view isn't cluttered while you're looking through the pod. Closing the TGP brings the HMD straight back (state preserved).
- **`NumPad 6`** — cross-system slew. HMD's current waypoint becomes the TGP's slew destination.
- **One profile file** — both subsystems read from the same `$profile:RR10_TGP/settings.json`. There's no separate HMD settings dialog; the TGP one covers both.

---

### ⌨️ Quick keybind chart

#### While in the pilot seat (TGP closed or open)

| Key | Action |
|---|---|
| `T` | Open / close the TGP camera |
| `Shift+H` | Toggle HMD on/off |
| `Shift+J` | Toggle IR sparkle (works even with TGP closed) |
| `Shift+O` | Cycle HMD waypoint mode (WP → RTE → TGT) |
| `NumPad 6` | Slew TGP to active HMD waypoint |
| `NumPad 7` | Set HMD waypoint by grid |
| `NumPad 8` | Set HMD waypoint by map pick |
| `NumPad 9` | Confirm map cursor as HMD waypoint |
| `Shift+C` | Cycle chalk sub-LZ (RTE mode) |
| `Shift+X` | Cycle destination type (RTE mode) |
| `Shift+N` | Force advance to next route leg (RTE mode) |
| `NumPad 5/4` *(hold)* | Smooth zoom in / out (when in smooth zone) |

#### While the TGP camera is open

| Key | Action |
|---|---|
| `NumPad 5` *(press)* | Step zoom in |
| `NumPad 4` *(press)* | Step zoom out (also cycles target slot — see below) |
| `G` | Slew to grid (opens dialog) |
| `Shift+M` | Slew to map (click, then `NumPad 1` to confirm) |
| `Y` | Drop a marker at the camera trace point |
| `Shift+Y` | Toggle marker label overlay |
| `Shift+L` | Toggle geolock |
| `Shift+N` | Toggle thermal / FLIR |
| `PageUp` / `PageDown` | Thermal gain up / down |
| `Shift+S` | Store current aim into the next target slot |
| `Shift+Tab` | Slew to selected target slot |
| `Shift+P` | Open settings dialog |
| `Shift+B` | Toggle BFT friendly overlay |
| `-` *(numpad minus)* | Re-center camera (forward, slight down) |

#### Notes on shared keys

- **`NumPad 4`** in the overlay context does two things at once: step zoom out, and cycle the selected target slot. The script picks the right action based on whether you have any target slots in use.
- **`Shift+N`** is both "force next route leg" (when HMD is up and you're in RTE mode) and "toggle FLIR" (when the TGP is up). Since the HMD hides whenever the TGP's up, these never conflict in practice.

---

### 🛠️ Troubleshooting

<details>
<summary><b>The TGP won't open even though I'm in the pilot seat.</b></summary>

Wait a second and a half after the seat fills. There's an intentional entry delay so you don't fire `T` accidentally while boarding.
</details>

<details>
<summary><b>I can't disembark.</b></summary>

The TGP blocks dismount while open. Press `T` to close it first.
</details>

<details>
<summary><b>My map clicks aren't doing anything.</b></summary>

You probably pressed `Shift+M` to open the map but haven't pressed `NumPad 1` to commit. Hover the cursor where you want and tap `NumPad 1`. Pressing `Shift+M` again closes without committing.
</details>

<details>
<summary><b>My TGP settings reset.</b></summary>

The settings file lives under your game profile at `$profile:RR10_TGP/settings.json`. If your profile moved or got wiped, defaults come back. The mod also bumps the file version when its schema changes — a one-time prompt-free migration that fills new fields with defaults; old custom values survive.
</details>

<details>
<summary><b>Sparkle isn't visible to other players.</b></summary>

Two things to check:
1. The receiving player needs night-vision goggles equipped to see the beam.
2. You have to be inside the dedicated-server render cap (1500 m default).
</details>

<details>
<summary><b>The CCIP pipper is gone.</b></summary>

A few possibilities:
- You're not armed with a weapon the mod recognizes (check the HMD — it should show the weapon's name, not `NO WEP`)
- The predicted impact is beyond 3 km
- It'd land behind the camera

The pipper hides rather than lie.
</details>

<details>
<summary><b>RTE-mode waypoint isn't showing anything.</b></summary>

The route needs `AFR <name>` and `CP <name> NN` markers on the map. They have to be your faction. The HMD reads the engine's map-marker list — anything you can see on your own map should be picked up. If you can't see them on your map either, they're not faction-visible to you.
</details>

---

## 📜 License & Credits

Original Aircraft Systems content is released under **APL**. See the [LICENSE](https://github.com/10thrangerregiment-dev/Aircraft-Systems?tab=License-1-ov-file) for full terms.

Dependencies retain their original licensing — see [CREDITS](https://github.com/10thrangerregiment-dev/Aircraft-Systems/blob/main/credits) for the full list.

## 💬 Community

Questions, bug reports, or want to help? Hop in the [Discord](https://discord.gg/YhQgs2ucGY) or open an issue on this repo.
