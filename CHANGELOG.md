## [2026-11-28] - Reduce metrics size; disable broken achievements
**What changed:** `README.md` renders `github-metrics.svg` at natural width `480` instead of `100%`; `.github/workflows/metrics.yml` sets `plugin_achievements: no`.
**Why:** `width="100%"` stretched the metrics image too large; `plugin_achievements: yes` currently renders `Unexpected error` because `lowlighter/metrics` queries sunset `user.projects` (Projects classic) instead of `user.projectsV2`. Pinning open PR #1834 failed while building the forked action image.
**Impact:** Metrics workflow succeeds without the `Achievements` error box; metrics image is smaller; re-enable `plugin_achievements` once upstream fixes `user.projects`.
