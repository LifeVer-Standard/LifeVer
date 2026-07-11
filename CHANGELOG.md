# Changelog

All notable changes to the LifeVer standard itself are documented here, using plain [SemVer](https://semver.org/) — not the `EPOCH.MILESTONE.STEP` scheme LifeVer defines for tracking a *person's* life. That scheme is for changelog authors; this file is the changelog for the standard they follow.

> **Note on 1.0–1.4:** These entries are reconstructed from the original design discussion that produced the standard, since no versioned drafts exist from that period — the spec was written up as a single "v1.4" document at the end of that conversation. From 1.4.1 onward, entries reflect actual merged changes.

## [1.5.0] - 2026-07-11

### Added
- **The MILESTONE Test** (Section 1): a two-part rule for the MILESTONE-vs-STEP boundary — sustained effort across multiple weeks/months *and* a lasting result, both required. Applies to `Added`/`Improved`/`Fixed`/`Removed`; `Changed` entries are tiered by severity instead (see below).
- **Private by Default, Curated by Choice** guiding principle (Section 6): the raw log is private by default, and sharing happens through separate curated derivatives, not by exposing the log itself.

### Changed
- Extended the **Honesty and Resilience** principle (Section 6): a `Changed` entry's tier is decided by severity and impact, not capped at STEP — a layoff or serious diagnosis can be exactly as version-significant as an achievement.

## [1.4.1] - 2026-07-11

### Changed
- Dropped the "often, but not required to be, aligned with your age" aside from the `EPOCH` definition. It was never load-bearing and quietly conflicted with EPOCH's own definition as an identity-altering event.
- Made the Section 5 allowance for retagging old entries after adding a new Scope explicit rather than implied.

### Added
- **Immutable History, Correctable Record** guiding principle (Section 6), distinguishing historical fact (immutable) from the changelog's classification of it (correctable).
- `LICENSE.md` (CC BY 4.0), matching what lifever.org already asserted.
- This file.

## [1.4.0] - 2025-06-06

### Added
- The `Changed` type, for logging significant life events that are neutral, negative, or externally imposed (a diagnosis, a layoff, a relocation) — without forcing them into the four agency-oriented types.
- Formal documentation of the full standard, including Appendix A for AI/automated parsing (regexes, entry delimiters, JSON data model).

## [1.3.0] - 2025-06-06

### Added
- Ratified `Added`, `Improved`, `Fixed`, `Removed` as a stable, closed list of Change Types — deliberately kept smaller and less mutable than Scopes, since the *kinds* of change in a life are more universal than its *domains*.

## [1.2.0] - 2025-06-06

### Added
- Formalized Scopes as an open, extensible list, with the "Rule of Three" as the guideline for when to add a new one.
- **Separation of Concerns** principle: to-do/issue-tracking stays in a separate tool entirely; the changelog only looks backward.

## [1.1.0] - 2025-06-06

### Added
- The `[Unreleased]` section as a low-friction capture buffer.
- The "Review & Release Ceremony" workflow, with Weekly recommended as the default cadence.
- Decided to keep a single unified changelog (not split by life domain) to preserve a holistic, cross-domain view.

## [1.0.0] - 2025-06-06

### Added
- Initial `EPOCH.MILESTONE.STEP` versioning scheme, adapted from Semantic Versioning.
- Initial four Change Types (`Added`, `Improved`, `Fixed`, `Removed`) and the `[Scope]` tag with a starting list of life domains.
