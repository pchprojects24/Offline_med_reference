# Offline Clinical Reference

A multi-file offline HTML clinical reference designed for use on iOS devices in the Readdle Documents app (or any local file browser). **No internet connection required.**

## Quick Start

1. **Copy** the entire `/OfflineClinicalRef/` folder to your device (e.g., via AirDrop, USB, or cloud sync)
2. **Open** in Readdle Documents (or similar app that can browse local HTML files)
3. **Navigate** to `/OfflineClinicalRef/index.html` and open it
4. **Use** the navigation buttons to access clinical references

## Folder Structure

```
OfflineClinicalRef/
├── index.html          ← START HERE (main landing page)
├── style.css           ← Shared styling
├── acls.html           ← ACLS menu
├── trauma.html         ← Trauma/ATLS (placeholder)
├── meds.html           ← Medications (placeholder)
├── procedures.html     ← Procedures (placeholder)
├── shipboard.html      ← Shipboard/At-Sea (placeholder)
├── evac.html           ← Evacuation (placeholder)
├── environmental.html  ← Environmental medicine (placeholder)
├── admin.html          ← Admin/Quick reference (placeholder)
├── acls/               ← ACLS algorithm pages
│   ├── shockable_vf_pvt.html        ← VF/pVT algorithm (READY)
│   ├── nonshockable_pea_asystole.html
│   ├── bradycardia.html
│   ├── tachycardia.html
│   ├── post_rosc.html
│   └── cardioversion.html
├── trauma/             ← Future trauma content
├── meds/               ← Future medication content
├── procedures/         ← Future procedure content
├── shipboard/          ← Future shipboard content
├── evac/               ← Future evacuation content
├── environmental/      ← Future environmental content
└── admin/              ← Future admin content
```

## Offline Rules (Non-Negotiable)

This reference is designed to work completely offline. The following rules ensure offline compatibility:

- **Relative links only** - No absolute paths (no leading `/`), no `http://` or `https://`
- **No external fonts** - Uses system fonts only (`-apple-system`, `BlinkMacSystemFont`, etc.)
- **No external scripts** - No CDNs, no JavaScript libraries
- **No external assets** - No images, fonts, or resources loaded from the internet
- **Self-contained CSS** - All styling is in `style.css` within the folder

## Entry Point

**New entry point:** `/OfflineClinicalRef/index.html`

The legacy single-file version (`offline_clinical_reference.html` in repo root) is preserved for reference but the multi-file structure in `/OfflineClinicalRef/` is the active version.

## Adding Content

When adding new content:

1. Create HTML files in the appropriate subfolder
2. Link using relative paths (e.g., `../acls.html` from within `/acls/`)
3. Include the shared stylesheet: `<link rel="stylesheet" href="../style.css">`
4. Add navigation with "Home" (`../index.html`) and section back links
5. Test offline by opening in a local browser with no network

## Mobile-First Design

- Large tap targets (minimum 44px height)
- High contrast dark theme
- Simple navigation with sticky headers
- Scrollable content panels

## Disclaimer

This is a personal quick reference tool. Always verify clinical content against current guidelines and local protocols. This reference is not a substitute for proper medical training or official clinical guidelines.
