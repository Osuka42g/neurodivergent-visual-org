---
created: 2025-11-02
updated: 2025-11-03T00:27
---
# User Preference Configuration

## Setting Your Default Mode

Create this file in your vault to set default mode:
`.claude/neurodivergent-visual-org-preference.yml`

```yaml
mode: neurodivergent  # Options: neurodivergent, neurotypical, auto-detect
time_buffer_multiplier: 1.5  # For neurodivergent mode: 1.5-2.0
chunk_size_max: 5  # Max items per section
color_scheme: calming  # Options: calming, standard, custom
```

## Quick Mode Override

In conversation:
- "Use neurotypical mode for this"
- "Switch to ADHD mode"
- "Auto-detect mode"

## Per-Diagram Settings

Some users may want mixed approaches:
- Neurodivergent mode for personal tasks
- Neurotypical mode for team presentations
- Auto-detect for general use
