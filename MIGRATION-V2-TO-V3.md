---
created: 2025-11-02
updated: 2025-11-03T00:37
---
# Migration Guide: v2.0 → v3.0

## Summary

v3.0 is **backward compatible** with v2.0. Existing users experience no breaking changes.

**Default behavior:** v3.0 defaults to neurodivergent mode (same as v2.0)

**New feature:** Optional neurotypical mode and auto-detection

## What Changed

### For Existing Users (No Action Required)

If you're happy with v2.0 behavior:
- ✅ Nothing changes
- ✅ Same neurodivergent-optimized diagrams
- ✅ Same compassionate language
- ✅ Same micro-steps and energy tracking
- ✅ All v2.0 patterns still work

### New Optional Features

**1. Neurotypical Mode**

Request it explicitly:
```
"Use neurotypical mode for this diagram"
"Create a professional version for my team"
```

**2. Auto-Detection**

Enable adaptive mode switching:
```
Create: .claude/neurodivergent-visual-org-preference.yml

mode: auto-detect
```

Now the skill adapts based on your language:
- Distress signals → Neurodivergent mode
- Professional requests → Neurotypical mode

**3. Mode Switching**

Switch mid-conversation:
```
"Make this more detailed" → Neurodivergent mode
"Make this more compact" → Neurotypical mode
```

## File Structure Changes

### v2.0 Structure
```
neurodivergent-visual-org-v2/
├── SKILL.md
├── README.md
└── references/
    ├── task-breakdowns.md
    ├── decision-tools.md
    └── ...
```

### v3.0 Structure
```
neurodivergent-visual-org-v3/
├── SKILL.md (updated with mode logic)
├── README.md (updated with mode docs)
├── config/
│   ├── modes.md (mode definitions)
│   └── user-preference.md (config guide)
├── templates/
│   ├── neurodivergent/ (v2.0 patterns moved here)
│   │   ├── task-breakdown.md
│   │   ├── decision-tree.md
│   │   └── ...
│   └── neurotypical/ (new templates)
│       ├── task-breakdown.md
│       ├── decision-tree.md
│       └── ...
├── examples/
│   └── mode-comparison.md
└── tests/
    └── test_mode_detection.md
```

**Migration:** Old `references/` files are now in `templates/neurodivergent/` with added frontmatter

## Configuration (Optional)

### Create Config File

If you want to customize behavior:

**File:** `.claude/neurodivergent-visual-org-preference.yml`

```yaml
# Mode options: neurodivergent, neurotypical, auto-detect
mode: neurodivergent  # v2.0 behavior (default)

# For neurodivergent mode: 1.5-2.0 recommended
time_buffer_multiplier: 1.5

# Max items per section (neurodivergent: 3-5, neurotypical: 5-7)
chunk_size_max: 5

# Color scheme: calming, standard
color_scheme: calming
```

### Use Auto-Detect

Enable intelligent mode switching:

```yaml
mode: auto-detect
```

Now you get:
- Neurodivergent mode when you're overwhelmed
- Neurotypical mode for professional requests
- Automatic adaptation to your current state

## API Changes

**SKILL.md changes:**
- Added mode detection section
- Added template selection logic
- Added mode switching guidance

**No breaking changes:**
- All v2.0 patterns still accessible
- Default behavior unchanged
- Reference files moved but still functional

## Testing Your Migration

### Verify v2.0 Behavior (Default)

**Test:** "I'm overwhelmed by cleaning my apartment"

**Expected:**
- ✅ Neurodivergent mode diagram
- ✅ 3-10 minute micro-steps
- ✅ Compassionate language
- ✅ Energy indicators
- ✅ Identical to v2.0 output

### Test New Features

**Test 1: Neurotypical Mode**
```
"Use neurotypical mode to create a project timeline"
```
Expected: Standard tasks, professional format

**Test 2: Mode Switching**
```
Turn 1: "I'm stuck on this project" (neurodivergent)
Turn 2: "Create a neurotypical version for my manager"
```
Expected: Both diagrams generated, differences explained

**Test 3: Auto-Detect**
```
Config: mode: auto-detect

"I'm paralyzed by this task list" → Neurodivergent
"Create Q4 roadmap" → Neurotypical
```

## Troubleshooting

### "Mode not working as expected"

**Check:**
1. Config file syntax (YAML formatting)
2. Explicit mode request clarity
3. Auto-detect keywords in your message

**Debug:**
```
"What mode are you using right now?"
"Switch to neurodivergent mode"
```

### "Prefer v2.0 behavior"

**Solution:** No action needed! v3.0 defaults to neurodivergent mode.

Optionally, lock it in config:
```yaml
mode: neurodivergent  # Disable auto-detect
```

### "Want to try auto-detect"

**Solution:**
```yaml
mode: auto-detect
```

Test with varied language:
- Distressed: "I'm overwhelmed..." → Neurodivergent
- Professional: "Create timeline..." → Neurotypical

## Rollback to v2.0

If needed:
```bash
/plugin install neurodivergent-visual-org@superpowers-marketplace --version 2.0.0
```

**Note:** v3.0 is backward compatible. Rollback shouldn't be necessary.

## Getting Help

- **Issues:** https://github.com/JackReis/neurodivergent-visual-org/issues
- **Discussions:** https://github.com/JackReis/neurodivergent-visual-org/discussions
- **Examples:** See `examples/mode-comparison.md`

## What's Next

After migrating:

1. **Test auto-detect** - See how it adapts to your language
2. **Try neurotypical mode** - For work presentations
3. **Customize config** - Fine-tune to your preferences
4. **Share feedback** - Help improve v3.1+

---

**Remember:** v3.0 defaults to the same compassionate, neurodivergent-optimized behavior as v2.0. New features are opt-in enhancements, not required changes. 💙
