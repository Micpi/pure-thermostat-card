# Pure Thermostat Card

Minimal thermostat Lovelace card inspired by Home Assistant native thermostat, with a clean circular UI and full visual editor.

## Features

- Circular thermostat dial
- Target and current temperature display
- Plus/minus controls
- HVAC mode buttons
- Visual editor with:
  - entity picker
  - icon picker
  - color pickers
  - style presets and layout options

## Installation

Add this repository in HACS as a Lovelace plugin.

## Lovelace Resource

```yaml
resources:
  - url: /hacsfiles/pure-thermostat-card/pure-thermostat-card.js
    type: module
```

## Basic Usage

```yaml
type: custom:pure-thermostat-card
entity: climate.living_room
name: Living Room
temperature_step: 0.5
style:
  preset: navbar_popup
  appearance: glass
  active_color: "#ff7a1a"
```

## Advanced Example

```yaml
type: custom:pure-thermostat-card
entity: climate.living_room
name: helper__wohnzimmer__thermostat_heizung
temperature_step: 0.5
precision: 1
show_current_temp: true
show_plus_minus: true
show_mode_buttons: true
mode_whitelist:
  - heat
  - off
style:
  preset: navbar_popup
  shape: rounded
  appearance: glass
  size: comfortable
  elevation: soft
  auto_text_contrast: true
  active_color: "#ff7a1a"
  inactive_color: "rgba(255,255,255,0.45)"
  background_color: "rgba(17,24,39,0.78)"
  text_color: "#f9fafb"
```
