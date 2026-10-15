# Western Occultism

A static, offline-friendly grimoire of interactive pages — no backend, no build step.
Open it in any phone or laptop browser.

| Module | Path |
| --- | --- |
| Portal (start here) | `index.html` |
| Tarot — Thoth deck, 78 cards | `modules/tarot/` |
| Planetary Hours — 90+ world cities or custom coordinates/time zone | `modules/planetary/` |
| Qabala — Tree of Life / Liber 777 | `modules/qabala/` |
| Alchemy — Liber Azoth | `modules/alchemy/` |
| LBRP — Lesser Banishing Ritual of the Pentagram | `modules/lbrp/` |

## View it online (GitHub Pages)

1. Push this repo to GitHub.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
3. After a minute the site is live at `https://<user>.github.io/<repo>/`.

## Run locally

The pages probe for each other with `fetch`, which browsers block on `file://`, so serve the folder:

```sh
python3 -m http.server 8000
```

then open <http://localhost:8000/>.

## Notes

- Planetary hours are computed entirely in the browser (NOAA solar algorithm + the browser's built-in
  time zone database). Pick a city or enter coordinates and an IANA time zone; the choice is remembered
  on that device. "Use my location" asks the browser for GPS and uses the device time zone.
