# NeuMorphix

A neumorphic theme for [Home Assistant](https://www.home-assistant.io/) that brings soft shadows, rounded surfaces, and a tactile 3D feel to your dashboards.

NeuMorphix ships with **6 theme variants** across two styles:

| Style | Light | Dark | Claude |
|-------|-------|------|--------|
| **Raised** | `neumorphix-light` | `neumorphix-dark` | `neumorphix-claude` |
| **Inset** | `neumorphix-light-inset` | `neumorphix-dark-inset` | `neumorphix-claude-inset` |

- **Raised** variants give cards and elements a soft, extruded look — the classic neumorphic style.
- **Inset** variants flip the effect so elements appear pressed into the surface.

> [!NOTE]
> **Inset themes and the Settings page**
>
> The inset theme variants do not apply to the main Settings page. The Settings page is part of Home Assistant's core UI and is rendered differently from dashboard views, which means theme tools like card-mod cannot reach it. Every other page — including all dashboard views and all Settings sub-pages — themes correctly.

## Prerequisites

- **Home Assistant** 2023.9.0 or newer
- **[card-mod](https://github.com/thomasloven/lovelace-card-mod)** — install it through HACS before installing NeuMorphix

## Installation

### HACS (recommended)

1. Open HACS in your Home Assistant instance.
2. Go to **Frontend** (the three-dot menu in the top right).
3. Select **Custom repositories**.
4. Add the URL of this repository and choose **Theme** as the category.
5. Search for **NeuMorphix** in HACS and install it.
6. Restart Home Assistant.

### Manual

1. Download the `themes/` folder from this repository.
2. Copy `neumorphix.yaml` and `neumorphix-inset.yaml` into your Home Assistant `config/themes/` directory.
3. Restart Home Assistant.

## Configuration

Make sure your `configuration.yaml` includes the frontend integration with the card-mod resource:

```yaml
frontend:
  themes: !include_dir_merge_named themes
  extra_module_url:
    - /hacsfiles/lovelace-card-mod/card-mod.js
```

After restarting, go to **Settings → General** and pick a NeuMorphix variant from the **Theme** dropdown — or set it per-dashboard in the dashboard settings.

## Theme variants

- `neumorphix-light` — light raised neumorphic
- `neumorphix-dark` — dark raised neumorphic
- `neumorphix-claude` — claude-inspired raised neumorphic
- `neumorphix-light-inset` — light inset neumorphic
- `neumorphix-dark-inset` — dark inset neumorphic
- `neumorphix-claude-inset` — claude-inspired inset neumorphic

## License

MIT
