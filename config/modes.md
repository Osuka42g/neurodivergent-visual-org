---
created: 2025-11-02
updated: 2025-11-03T00:27
---
# Mode Configuration Reference

## Available Modes

### Neurodivergent Mode (Default)

**Optimized for:** ADHD, autism, executive dysfunction, decision paralysis, time blindness

**Characteristics:**
- Information chunks: 3-5 per section (ADHD working memory)
- Time estimates: 1.5-2x standard with buffer
- Color scheme: Calming (blues, greens, muted tones)
- Language: Compassionate, non-judgmental
- Scaffolding: Energy awareness, permission statements, anti-perfectionism
- Task granularity: 3-10 minute micro-steps
- Visual density: Low (reduce overstimulation)

### Neurotypical Mode

**Optimized for:** Standard executive function, occasional need for structure, complex project planning

**Characteristics:**
- Information chunks: 5-7 per section (Miller's Law)
- Time estimates: Standard (no buffer)
- Color scheme: Standard Mermaid themes
- Language: Direct, efficient
- Scaffolding: Minimal
- Task granularity: 15-30 minute tasks
- Visual density: Medium-high (information efficient)

### Auto-Detect Mode

**Behavior:** Analyzes user language and context to select appropriate mode

**Triggers for Neurodivergent Mode:**
- Keywords: "overwhelmed", "paralyzed", "stuck", "can't decide", "don't know where to start"
- Mentions: "ADHD", "autism", "executive dysfunction", "time blindness", "decision paralysis"
- Energy mentions: "spoons", "burned out", "exhausted", "no energy"

**Triggers for Neurotypical Mode:**
- Direct requests: "quick breakdown", "efficient", "high-level"
- Professional context: "team", "meeting", "presentation", "stakeholder"
- No distress signals in language

**Default if ambiguous:** Neurodivergent mode (inclusive design principle)

## Mode Switching

Users can switch modes:
1. Explicitly: "Use neurotypical mode" or "Use ADHD mode"
2. Mid-conversation: "Can you make this more detailed?" or "Can you simplify this?"
3. Configuration file: Set preferred default mode

## Backward Compatibility

v3.0 defaults to neurodivergent mode to maintain v2.0 behavior.
