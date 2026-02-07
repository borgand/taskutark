# Taskutark - Estonian Educational Kiosk

Educational landing page and kiosk configuration for Estonian schools. Provides students with curated access to study resources while restricting non-educational websites.

## What's Included

- **[landing-page.html](landing-page.html)** - Curated educational portal in Estonian
- **[kiosk-config.xml](kiosk-config.xml)** - Kiosk Pro configuration with domain whitelist

## Setup

1. **Enable GitHub Pages** on this repository (Settings → Pages → Deploy from branch `main`)
2. **Import configuration** in Kiosk Pro app using:
   ```
   https://borgand.github.io/taskutark/kiosk-config.xml
   ```

The landing page will be available at: `https://borgand.github.io/taskutark/landing-page.html`

## Features

### Landing Page
- Primary study platforms (Stuudium, Opiq)
- Reference resources (Wikipedia, Sõnaveeb, Google Translate)
- Learning tools (Khan Academy, Desmos, GeoGebra, WolframAlpha)
- Estonian educational materials (e-Koolikott, Haridusportaal)

### Kiosk Settings
- Domain whitelist (educational sites only)
- Remote config updates (every 5 minutes)
- Idle timer (returns to homepage after 5 min)
- Passcode-protected settings (default: `1234`)
- Cookie retention for login persistence

## Customization

**Add allowed domain**: Edit `kiosk-config.xml` under `kp_allowedDomains`
```xml
<string>newsite.com</string>
```

**Change passcode**: Edit line 34 in `kiosk-config.xml`

**Modify links**: Edit `landing-page.html`

## Requirements

- Kiosk Pro app (iOS/iPadOS)
- GitHub Pages enabled
- iPad for deployment
