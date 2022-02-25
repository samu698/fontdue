# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]
### Fixed
- `LinePosition` doc typo.

## [0.7.0] - 2022-02-25
### Added
- A changelog.
- `simd` flag, enabled by default. Leverages simd functions. This was implicitly always enabled prior.
- `parallel` flag, disabled by default. Uses `std` + `rayon` to thread font loading.
- `Font.chars()` gets all valid unicode codepoints that have mappings to glyph geometry in the font.
- `LinePosition` holds various metadata on positioned lines computed during layout.
### Changed
- `Layout.lines()` returns a `Option<Vec<LinePosition>>` now instead of a line count.