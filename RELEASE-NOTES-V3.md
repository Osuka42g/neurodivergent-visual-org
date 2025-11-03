---
created: 2025-11-02
version: 3.0.0
updated: 2025-11-03T00:37
---
# Release Notes: v3.0 - Adaptive Cognitive Modes

## TL;DR

v3.0 adds neurotypical/neurodivergent mode toggle with auto-detection. Use ADHD mode for personal planning, NT mode for team presentations, or let it auto-detect based on your language.

**Backward compatible:** Defaults to neurodivergent mode (v2.0 behavior)

## What's New

### 🎯 Mode Toggle System

Three modes to match your needs:

**1. Neurodivergent Mode (Default)**
- 3-5 item chunks (ADHD working memory)
- 1.5-2x time buffers
- 3-10 minute micro-steps
- Compassionate language
- Energy indicators (⚡)
- Break reminders
- Permission statements

**2. Neurotypical Mode (Opt-In)**
- 5-7 item chunks (Miller's Law)
- Standard time estimates
- 15-30 minute tasks
- Direct, professional language
- Efficient layout
- Minimal scaffolding

**3. Auto-Detect Mode**
- Analyzes your language
- Distress signals → Neurodivergent
- Professional requests → Neurotypical
- Ambiguous → Neurodivergent (inclusive default)

### 🧩 Dual Template System

Separate pattern libraries for each cognitive style:

```
templates/
├── neurodivergent/  (v2.0 patterns + mode frontmatter)
│   ├── task-breakdown.md
│   ├── decision-tree.md
│   ├── project-map.md
│   └── ...8 total
└── neurotypical/  (new professional templates)
    ├── task-breakdown.md
    ├── decision-tree.md
    ├── project-map.md
    └── ...3 core templates
```

### ⚙️ Configuration System

Set your preferences:

`.claude/neurodivergent-visual-org-preference.yml`
```yaml
mode: auto-detect  # neurodivergent, neurotypical, auto-detect
time_buffer_multiplier: 1.5
chunk_size_max: 5
color_scheme: calming
```

### 🔄 Mode Switching

Change modes mid-conversation:

```
Turn 1: "I'm overwhelmed by this project"
→ Neurodivergent mode: micro-steps, compassionate

Turn 2: "Create a neurotypical version for my manager"
→ Neurotypical mode: professional, efficient
```

### 📚 New Documentation

- **config/modes.md** - Mode definitions and characteristics
- **config/user-preference.md** - Configuration guide
- **examples/mode-comparison.md** - Side-by-side mode examples
- **tests/test_mode_detection.md** - 10 test scenarios
- **MIGRATION-V2-TO-V3.md** - Upgrade guide
- **COMMUNITY-POSTS-V3.md** - v3-specific messaging

## Use Cases

### Personal Planning (Neurodivergent Mode)
```
You: "I'm paralyzed by my messy apartment"
→ 3-min micro-steps, energy tracking, compassionate support
```

### Team Presentations (Neurotypical Mode)
```
You: "Create a neurotypical version for stakeholders"
→ Professional format, standard tasks, efficient layout
```

### Auto-Adapt (Auto-Detect Mode)
```
Config: mode: auto-detect

"I'm overwhelmed..." → Neurodivergent
"Create Q4 roadmap" → Neurotypical
```

### Mixed Teams
```
Person A (ADHD): "I'm stuck on this task"
→ Neurodivergent: micro-steps, compassionate

Person B (NT): "Show me the project timeline"
→ Neurotypical: standard format
```

## Backward Compatibility

✅ **No breaking changes**

v3.0 defaults to neurodivergent mode (same as v2.0):
- Existing users: no action required
- Same compassionate diagrams
- Same micro-steps and energy tracking
- All v2.0 patterns still work

v2.0 files moved to `templates/neurodivergent/` (accessible via SKILL.md)

## Installation

### New Users
```bash
/plugin install neurodivergent-visual-org@superpowers-marketplace
```

### Existing Users (Auto-Update)
```bash
/plugin update neurodivergent-visual-org
```

## Migration from v2.0

See [MIGRATION-V2-TO-V3.md](MIGRATION-V2-TO-V3.md) for details.

**Quick summary:**
1. Update plugin (v3.0 defaults to v2.0 behavior)
2. No action required for existing workflow
3. Optionally enable auto-detect or neurotypical mode
4. Optionally create config file for preferences

## Testing v3.0

### Test Default Behavior (v2.0 Compatible)
```
"I'm overwhelmed by cleaning my apartment"
→ Should generate neurodivergent mode (micro-steps, compassionate)
```

### Test Neurotypical Mode
```
"Use neurotypical mode to create a project timeline"
→ Should generate professional, standard-task format
```

### Test Auto-Detect
```
Config: mode: auto-detect

"I'm paralyzed by this task list" → Neurodivergent
"Create team presentation" → Neurotypical
```

### Test Mode Switching
```
Turn 1: "Break down this overwhelming project" → Neurodivergent
Turn 2: "Now create a neurotypical version" → Both diagrams
```

## Known Issues

None (new release)

## Roadmap (v4.0 Ideas)

- Custom modes (user-defined templates)
- Team templates (share mode configs)
- Integration APIs (connect to task managers)
- Advanced auto-detect (learn user patterns)
- Multi-language support

## Community

- **Repository:** https://github.com/JackReis/neurodivergent-visual-org
- **Issues:** Report bugs or request features
- **Discussions:** Share use cases and feedback
- **Contributing:** PRs welcome (see CONTRIBUTING.md)

## Credits

Built with compassion for the neurodivergent community.

**Special thanks:**
- v2 users who requested neurotypical mode
- ADHD/autism communities for ongoing feedback
- Claude Code team for skills framework
- Mermaid.js team for diagramming library

## License

MIT License - Free and open source

---

**Remember:** v3.0 works WITH your brain, not against it. Choose the mode that helps you right now - whether that's compassionate micro-steps or efficient professional format. You're in control. 💙
