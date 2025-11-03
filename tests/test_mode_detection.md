---
created: 2025-11-02
type: test-scenarios
updated: 2025-11-03T00:30
---
# Mode Detection Test Scenarios

## Test 1: Explicit Neurodivergent Mode Request

**Input:** "Use ADHD mode to break down cleaning my apartment"

**Expected Mode:** neurodivergent

**Expected Behavior:**
- 3-5 minute micro-steps
- Compassionate language ("You've got this!")
- Energy indicators (⚡)
- Break reminders
- Permission statements

**Verification:**
```bash
✓ Mode detected: neurodivergent
✓ Chunk size: ≤5 items per section
✓ Time estimates include buffer (1.5-2x)
✓ Language contains validation phrases
✓ Diagram includes break points
```

---

## Test 2: Explicit Neurotypical Mode Request

**Input:** "Use neurotypical mode to create a project timeline"

**Expected Mode:** neurotypical

**Expected Behavior:**
- 15-30 minute tasks
- Direct, professional language
- Standard time estimates
- Efficient layout
- No emotional scaffolding

**Verification:**
```bash
✓ Mode detected: neurotypical
✓ Chunk size: 5-7 items per section
✓ Time estimates: standard (no buffer)
✓ Language: direct and professional
✓ No break points or permission statements
```

---

## Test 3: Auto-Detect Neurodivergent (Distress Signals)

**Input:** "I'm so overwhelmed by this project, I don't know where to start"

**Expected Mode:** neurodivergent (auto-detected)

**Keywords Detected:** "overwhelmed", "don't know where to start"

**Verification:**
```bash
✓ Distress keywords found: ["overwhelmed", "don't know where to start"]
✓ Mode auto-selected: neurodivergent
✓ Compassionate response generated
✓ Micro-steps applied
```

---

## Test 4: Auto-Detect Neurodivergent (Condition Mention)

**Input:** "My ADHD makes it hard to plan this project"

**Expected Mode:** neurodivergent (auto-detected)

**Keywords Detected:** "ADHD"

**Verification:**
```bash
✓ Neurodivergent condition mentioned: "ADHD"
✓ Mode auto-selected: neurodivergent
✓ ADHD-optimized template used
```

---

## Test 5: Auto-Detect Neurodivergent (Energy Mention)

**Input:** "I'm out of spoons, can you help me prioritize?"

**Expected Mode:** neurodivergent (auto-detected)

**Keywords Detected:** "spoons"

**Verification:**
```bash
✓ Energy-aware language detected: "spoons"
✓ Mode auto-selected: neurodivergent
✓ Energy-aware diagram generated
```

---

## Test 6: Auto-Detect Neurotypical (Straightforward)

**Input:** "Create a timeline for the Q4 product launch"

**Expected Mode:** neurotypical (auto-detected)

**Keywords Detected:** None (professional, straightforward request)

**Verification:**
```bash
✓ No distress signals found
✓ Professional context detected
✓ Mode auto-selected: neurotypical
✓ Standard project timeline generated
```

---

## Test 7: Mode Switching Mid-Conversation

**Conversation Flow:**

**Turn 1:**
User: "I'm paralyzed by this task list"
Expected: neurodivergent mode

**Turn 2:**
User: "Now create a neurotypical version for my manager"
Expected: Switch to neurotypical mode

**Verification:**
```bash
✓ Turn 1: neurodivergent mode (keyword: "paralyzed")
✓ Turn 2: neurotypical mode (explicit request)
✓ Both diagrams generated
✓ Explanation of differences provided
```

---

## Test 8: Ambiguous Input (Default Neurodivergent)

**Input:** "Help me plan my weekend"

**Expected Mode:** neurodivergent (default when ambiguous)

**Reasoning:** Inclusive design - default to more supportive mode

**Verification:**
```bash
✓ No clear mode indicators found
✓ Defaulted to: neurodivergent
✓ User can request neurotypical if preferred
```

---

## Test 9: Configuration File Override

**Config File:** `.claude/neurodivergent-visual-org-preference.yml`
```yaml
mode: neurotypical
```

**Input:** "Break down apartment cleaning"

**Expected Mode:** neurotypical (config override)

**Verification:**
```bash
✓ Config file detected
✓ Default mode: neurotypical (from config)
✓ Neurotypical template used
✓ Can still override with explicit request
```

---

## Test 10: Stress Context (Neurotypical User)

**Input:** "I'm burned out and this work project feels impossible"

**Expected Mode:** neurodivergent (even for neurotypical users)

**Reasoning:** Stress/burnout impairs executive function regardless of neurotype

**Verification:**
```bash
✓ Burnout keyword detected: "burned out"
✓ Distress signal: "feels impossible"
✓ Mode selected: neurodivergent
✓ Compassionate support provided
```

---

## Manual Testing Checklist

- [ ] Test 1: Explicit neurodivergent mode request
- [ ] Test 2: Explicit neurotypical mode request
- [ ] Test 3: Auto-detect neurodivergent (distress)
- [ ] Test 4: Auto-detect neurodivergent (condition)
- [ ] Test 5: Auto-detect neurodivergent (energy)
- [ ] Test 6: Auto-detect neurotypical (straightforward)
- [ ] Test 7: Mode switching mid-conversation
- [ ] Test 8: Ambiguous input defaults to neurodivergent
- [ ] Test 9: Configuration file override
- [ ] Test 10: Stress context (neurotypical user)

## Regression Tests (v2.0 Compatibility)

- [ ] Default behavior matches v2.0 (neurodivergent mode)
- [ ] All v2.0 patterns still work
- [ ] Existing reference files accessible via templates/neurodivergent/
- [ ] No breaking changes for users who don't configure modes
