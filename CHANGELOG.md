## [2026-11-28] - Fix achievements and reduce metrics size
**What changed:** `.github/workflows/metrics.yml` pins `ShawnXxy/metrics@1e49d0b8b932624dd7762147e35ccc137eda09f1` (PR #1834) to migrate achievements from sunset `user.projects` to `user.projectsV2`; `README.md` renders `github-metrics.svg` at natural width `480` instead of `100%`.
**Why:** GitHub Projects classic is sunset, causing `Achievements` to render `Unexpected error`; `width="100%"` stretched the metrics image too large.
**Impact:** Achievements should render; metrics image is smaller; no token or README section changes.
