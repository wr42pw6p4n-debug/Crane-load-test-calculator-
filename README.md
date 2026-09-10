# Key Engineering — Load Test Certification

A self-contained web app for recording overhead crane beam and swing jib load
tests, and generating printable test certificates. Built for **Key
Engineering (Chesterfield) Ltd**.

Open `index.html` in any browser — no install, no server, no build step.
All data (saved certificates, certificate numbering, company details) is
stored locally in the browser you use it in.

## Features

- **Two test types** — Overhead Crane Beam and Swing Jib — using the
  tolerance / deflection / test-load formulas from the original Key
  Engineering Excel calculators:
  - Crane beam tolerance = beam length ÷ 500
  - Swing jib tolerance = (beam length + no-load deflection) ÷ 250
  - Deflection under load = no-load reading − with-load reading
  - Required test load = SWL × 1.25
- **Live results readout** while you type, with a pass/fail gauge.
- Flags when the applied test load is below the required 125% SWL test load.
- Tracks residual deflection (post-test vs no-load) as a permanent-set check.
- **Generates a printable certificate** with auto-numbered references
  (`KE-CB-0001`, `KE-SJ-0001`, …), ready for "Print / Save as PDF".
- **Certificate Store** — every saved certificate stays on-device, searchable
  and filterable, with reprint and delete.
- Company name / address / phone / email are editable in-app (**Company
  details**) and appear on every certificate footer.

## Running it

Just open `index.html` — locally, or hosted anywhere that serves static
files (including GitHub Pages, see below).

## Hosting on GitHub Pages (optional)

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`.
4. Your app will be live at `https://<your-username>.github.io/<repo-name>/`.

## Icon

`assets/icon.svg` (plus PNG exports at 512/256/192/32px) — a monogram of
"KE" over a simply-supported beam under load, in the app's navy/orange
palette. Used as the in-app favicon and suitable as the repo's social image
or a home-screen icon.

## Notes

- Uprate/downrate figures are left as manual entry fields, matching the
  original calculators — they require engineering judgement, not a formula.
- No data leaves the browser; there is no backend.
