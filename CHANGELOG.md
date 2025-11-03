---
created: 2025-11-03T00:36
updated: 2025-11-03T00:37
---
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [3.0.0] - 2025-11-02

### Added

- **Neurotypical/Neurodivergent Mode Toggle** - Three modes: neurotypical, neurodivergent, auto-detect
- **Dual Template System** - Separate pattern libraries for each cognitive style
- **Auto-Detection** - Intelligent mode selection based on user language analysis
- **Configuration System** - User preference file for default mode and parameters
- **Mode Switching** - Mid-conversation mode changes with explanation
- **Neurotypical Templates** - Task breakdowns, decision trees, project maps optimized for standard executive function
- **Mode Comparison Examples** - Side-by-side demonstrations of each mode
- **Migration Guide** - Comprehensive v2→v3 upgrade documentation
- **Test Scenarios** - 10 mode detection test cases

### Changed

- **File Structure** - References moved to `templates/neurodivergent/` with mode frontmatter
- **SKILL.md** - Added mode detection algorithm and template selection logic
- **README.md** - Added mode configuration and quick reference sections
- **Plugin Manifest** - Updated description to highlight adaptive modes
- **Community Posts** - v3-specific messaging emphasizing inclusive toggle

### Deprecated

- None (v2.0 patterns remain accessible in `templates/neurodivergent/`)

### Removed

- None (backward compatible)

### Fixed

- None (new release)

### Security

- None

---

## [2.0.0] - 2025-11-02

### Added

- Comprehensive Mermaid 11.12.1 coverage (22 diagram types)
- Research-backed design principles (ADHD neuroscience, cognitive load theory)
- WCAG 2.1 accessibility compliance (4.5:1 contrast ratios)
- Comprehensive troubleshooting guide
- 6 detailed scenario examples
- Anti-patterns section
- Scientific foundation documentation

### Changed

- SKILL.md expanded from 143 to 984 lines
- README.md updated with v2 features
- All reference files enhanced with research citations

---

## [1.0.0] - 2025-11-03

### Added

- Initial release with 8 pattern libraries
- Neurodivergent-optimized Mermaid diagrams
- Compassionate language and micro-steps
- Energy-aware planning
- Task breakdowns, decision tools, project maps, current state boards, time-boxing, habit building, accountability support, focus regulation
- MIT License
- Plugin manifest for Claude Code
- GitHub repository

---

## Versioning Strategy

- **Major (X.0.0)** - Breaking changes or significant new features
- **Minor (x.Y.0)** - Backward-compatible new features
- **Patch (x.y.Z)** - Backward-compatible bug fixes

## v3.0.0 Rationale

Major version bump because:
1. Significant new feature (mode toggle system)
2. File structure reorganization (though backward compatible)
3. New configuration system
4. Architectural change (dual template system)

**Note:** Despite major version, v3.0.0 is backward compatible with v2.0
