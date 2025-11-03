---
created: 2025-11-02T22:59
updated: 2025-11-03T00:30
---
# Neurodivergent Visual Organization Skill v3.0

Upgraded skill for creating ADHD-friendly visual organizational tools using Mermaid diagrams with adaptive cognitive mode toggle.

## What's New in v3.0

### Major Enhancements

1. **Neurotypical/Neurodivergent Mode Toggle**
   - Three modes: neurotypical, neurodivergent, auto-detect
   - Automatic language detection for optimal mode
   - Explicit mode switching support
   - User configuration preferences

2. **Dual Template System**
   - Separate template libraries for each cognitive style
   - Neurotypical: 5-7 chunks, standard times, efficient layout
   - Neurodivergent: 3-5 chunks, buffered times, compassionate language
   - Mode-specific color schemes and scaffolding

3. **Enhanced Flexibility**
   - Use neurodivergent mode for personal planning
   - Switch to neurotypical mode for team presentations
   - Auto-detect adapts to user's current state
   - Mid-conversation mode switching

4. **Inclusive Design**
   - Neurotypical users benefit during stress/burnout
   - Teams can use same tool with different modes
   - Educational: demonstrates cognitive accessibility
   - Backward compatible (defaults to neurodivergent)

## Mode Quick Reference

| Need | Recommended Mode |
|------|------------------|
| Personal task overwhelm | Neurodivergent (auto-detects) |
| Team presentation | Neurotypical (request explicitly) |
| Executive dysfunction support | Neurodivergent |
| Standard project planning | Neurotypical |
| Mixed team collaboration | Auto-detect (adapts per person) |
| Stress/burnout (any neurotype) | Neurodivergent |

## Installation

### For Claude.ai Desktop (MCP Skills)

1. Locate your skills directory (usually `~/Library/Application Support/Claude/skills/user/`)
2. Backup existing `neurodivergent-visual-org` folder (if present)
3. Copy the `neurodivergent-visual-org-v3` folder contents to:
   - `~/Library/Application Support/Claude/skills/user/neurodivergent-visual-org/`
4. Restart Claude.ai Desktop app
5. Skill will be automatically available

### For Manual Use

Simply reference the `SKILL.md` file when creating ADHD-friendly visualizations. The reference files in the `templates/` directory provide additional patterns and examples.

## Configuring Your Mode

### Auto-Detect (Default)

The skill automatically chooses the best mode based on your language:
- Distress signals → Neurodivergent mode
- Straightforward requests → Neurotypical mode
- Ambiguous → Neurodivergent mode (inclusive default)

### Explicit Mode Request

In conversation:
```
"Use neurotypical mode for this diagram"
"Switch to ADHD mode"
"Make it more detailed" (switches to neurodivergent)
"Make it more compact" (switches to neurotypical)
```

### Set Default Mode

Create: `.claude/neurodivergent-visual-org-preference.yml`

```yaml
mode: auto-detect  # Options: neurotypical, neurodivergent, auto-detect
time_buffer_multiplier: 1.5  # For neurodivergent: 1.5-2.0
chunk_size_max: 5  # Max items per section
color_scheme: calming  # Options: calming, standard
```

## Package Contents

```
neurodivergent-visual-org-v3/
├── SKILL.md                          # Main skill file with mode detection
├── README.md                         # This file
├── config/                           # Mode configuration
│   ├── modes.md                      # Mode definitions
│   └── user-preference.md            # Configuration guide
├── templates/                        # Template libraries
│   ├── neurodivergent/               # ADHD-optimized (v2.0 patterns)
│   │   ├── task-breakdown.md
│   │   ├── decision-tree.md
│   │   ├── project-map.md
│   │   ├── current-state.md
│   │   ├── time-boxing.md
│   │   ├── habit-building.md
│   │   ├── accountability.md
│   │   └── focus-regulation.md
│   └── neurotypical/                 # Professional templates
│       ├── task-breakdown.md
│       ├── decision-tree.md
│       └── project-map.md
├── examples/                         # Mode comparison examples
│   └── mode-comparison.md
└── tests/                            # Test scenarios
    └── test_mode_detection.md
```

## Quick Start

The skill activates when users:
- Feel overwhelmed by tasks
- Experience decision paralysis
- Need to break down complex projects
- Struggle with time blindness
- Want to track habits or energy
- Need visual organization tools
- Request professional presentations

### Example Usage

**User:** "I need to clean my apartment but it's so messy I don't know where to start"

**Skill Response:**
1. Auto-detects neurodivergent mode (keywords: "so messy", "don't know where to start")
2. Creates flowchart or timeline breaking cleaning into 10-15 minute chunks
3. Starts with "quick wins" for visible progress
4. Uses calming color theme
5. Includes validation and encouragement
6. Renders with Mermaid tool
7. Offers to save to Obsidian

## Key Principles

### Neurodivergent Mode
- **Compassionate language** (never "just" or "should")
- **Realistic time estimates** (1.5-2x normal estimates)
- **Energy awareness** (acknowledge spoon theory)
- **Micro-steps** (3-10 minute tasks)
- **Permission statements** (combat perfectionism)
- **Celebrate starting** (not just finishing)
- **3-5 information chunks** per section (working memory)
- **Calming colors** (blues, greens, muted tones)

### Neurotypical Mode
- **Direct language** (efficient, professional)
- **Standard time estimates** (no buffer)
- **Standard tasks** (15-30 minute blocks)
- **Professional presentation** (stakeholder-ready)
- **5-7 information chunks** per section (Miller's Law)
- **Standard color schemes** (Mermaid defaults)

## Mermaid Quick Reference

### Most Useful Diagram Types for ADHD

| Need | Diagram Type |
|------|--------------|
| "I don't know where to start" | Flowchart (decision tree) |
| "This is overwhelming" | Timeline or Gantt chart |
| "I can't decide" | Quadrant chart (Eisenhower Matrix) |
| "What should I focus on?" | Quadrant chart or Pie chart |
| "Time disappears" | Timeline (make time visible) |
| "No energy" | Pie or Sankey (spoon theory) |
| "Build a habit" | Flowchart or User journey |

### Cognitive Load Limits

**Neurodivergent Mode:**
- **Flowcharts**: 12-15 nodes maximum
- **Mindmaps**: 2-3 levels deep
- **Pie charts**: 4-6 slices
- **Lists**: 2 lists × 3-5 items max
- **Sections**: 3-5 per diagram

**Neurotypical Mode:**
- **Flowcharts**: 20-25 nodes maximum
- **Mindmaps**: 4-5 levels deep
- **Pie charts**: 6-8 slices
- **Lists**: 2 lists × 5-7 items max
- **Sections**: 5-7 per diagram

### Recommended Themes

**Neurodivergent Mode:**
- `forest` - Calming green-based
- `neutral` - Muted earth tones
- Both reduce visual overstimulation

**Neurotypical Mode:**
- `default` - Standard Mermaid theme
- Any professional color scheme

## Troubleshooting

### Common Issues

**Diagram won't render**
- Check indentation consistency (mindmaps, composites)
- Avoid lowercase "end" as state name (use "End" or "END")
- Verify coordinates are 0-1 for quadrant charts
- Remove `::icon()` syntax for GitHub compatibility

**Colors not working**
- Use YAML frontmatter for Sankey config (not directives)
- Remember pie chart colors assigned by size, not order

**Events missing in timeline**
- All events before first `section` are ignored
- Add section before any timeline events

**Mode not detected correctly**
- Use explicit mode request: "Use neurotypical mode"
- Check configuration file syntax
- See test scenarios in `tests/test_mode_detection.md`

## Support & Resources

- **Reddit r/ADHD** - Community-shared patterns
- **ADDitude Magazine** - Research-backed strategies
- **CHADD** - Evidence-based resources
- **Mermaid Live Editor** - mermaid.live for testing
- **GitHub Repository** - Issues and discussions

## Version History

- **v3.0** - Neurotypical/neurodivergent mode toggle, dual template system, auto-detection
- **v2.0** - Comprehensive Mermaid syntax, research-backed design, troubleshooting
- **v1.0** - Initial release with basic patterns

## License

This skill incorporates research from neuroscience, cognitive psychology, and ADHD communities. Use freely and adapt to your needs.

---

**Remember**: Visual tools work WITH brain differences, not against them. These diagrams externalize executive function and make the invisible visible. Choose the mode that helps you right now.
