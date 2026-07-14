# ⚓ Abeam

**A Canadian mariner's pocket reference — [jessehawbolt.github.io/abeam](https://jessehawbolt.github.io/abeam/)**

Abeam is a lightweight, offline-first web app for professional Canadian mariners and students. It's built for quick access on watch: open it, find the channel, script, or table you need, and get back to the window.

> ⚠️ **Reference & training aid only.** Abeam is not an official publication and must not be relied upon for navigation, collision avoidance, or emergency procedures. Always verify against the current Seaway Handbook, RAMN, charts, and Notices to Mariners, and follow your vessel's procedures.

## Install on a phone

1. Open **https://jessehawbolt.github.io/abeam/** in Safari (iPhone) or Chrome (Android)
2. **Add to Home Screen** (Share menu on iOS, ⋮ menu on Android)
3. That's it — Abeam works fully offline after the first visit. Updates arrive automatically the next time you open it with a connection.

## What's inside

- **📻 Radio** — MAYDAY / PAN PAN / SÉCURITÉ fill-in scripts, Canadian VHF channel table, phonetic alphabet with Morse, figures and prowords
- **📍 CIPs** — St. Lawrence Seaway calling-in table (upbound & downbound, all sectors and stations), Great Lakes listening-watch table, Sarnia Traffic zone/areas with all calling-in points, Soo Traffic, and the standard VTS report designators A–Z
- **🛟 Buoyage** — IALA Region B laterals, bifurcations, cardinals with light rhythms, isolated danger / safe water / special marks, and Canadian inland hazard & control buoys
- **🧮 Tools** — CIP-to-CIP passage times for the Detroit & St. Clair rivers (speed-based, with ETAs), speed/distance/time calculator, marine unit converter, Beaufort scale, watchkeeping rules of thumb
- **🎓 Learning** — Transport Canada–style exam quiz (COLREGs, buoyage, radio, safety) and a full COLREGs quick reference: lights, day shapes, sound signals, right-of-way
- **🔴 Night mode** — red-on-black theme to preserve night vision on watch, plus day and dusk themes

## Sources

Content compiled from the **Seaway Handbook — Practices and Procedures** (March 2026, Schedule III & ss. 60–65), **Radio Aids to Marine Navigation 2026** (Annual Edition v5, ss. 3.4 & 3.9, Tables 3-31 to 3-34), **SOR/84-335**, **33 CFR 161.45**, and **TP 968** (The Canadian Aids to Navigation System). These publications are amended through the season — the app states its data vintage on the home page.

## Development

No build step, no dependencies: the whole app is `index.html` (vanilla HTML/CSS/JS), plus `sw.js` (offline cache), `manifest.json`, and `icon.svg`. Serve the folder with any static file server to develop locally:

```
python3 -m http.server 8123
```

When changing content, bump the cache version string at the top of `sw.js` — installed copies keep serving their cached version until it changes.

**Version 0.1 (alpha)** — July 2026
