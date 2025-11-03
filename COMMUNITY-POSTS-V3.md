---
created: 2025-11-02
updated: 2025-11-03T00:37
---
# Community Posts for Neurodivergent Visual Organization Skill v3.0

## Reddit - r/ADHD

**Title:** [Update] ADHD visual organization tool now has neurotypical mode toggle (v3.0)

**Post:**

Hey everyone,

Quick update on the Claude Code plugin I shared for breaking down overwhelming tasks into ADHD-friendly visual diagrams.

**New in v3.0: Mode Toggle**

The most-requested feature: you can now toggle between neurodivergent and neurotypical modes!

**Why this matters:**

**For personal use:**
- Use ADHD mode when you're overwhelmed ("I don't know where to start")
- Auto-switches to compassionate micro-steps, energy indicators, break reminders

**For team/work:**
- Switch to neurotypical mode for presentations to managers/colleagues
- Same project, two formats: one for you, one for neurotypicals

**For mixed teams:**
- Auto-detect mode adapts to each person's language
- Your coworker gets efficient format, you get supportive format
- Same tool, different modes

**How it works:**

**Auto-Detect (Default):**
```
You: "I'm so overwhelmed by cleaning my apartment"
→ ADHD mode: 3-min micro-steps, compassionate language, energy tracking

You: "Create a timeline for the Q4 launch"
→ Neurotypical mode: standard tasks, professional format
```

**Explicit Override:**
```
"Use ADHD mode for this"
"Switch to neurotypical mode for my presentation"
"Make it more detailed" (→ ADHD mode)
"Make it more compact" (→ neurotypical mode)
```

**Mode Comparison:**

| Aspect | ADHD Mode | Neurotypical Mode |
|--------|-----------|-------------------|
| Task size | 3-10 min | 15-30 min |
| Language | "You've got this!" | Direct, professional |
| Time estimates | 2x buffer | Standard |
| Energy tracking | Explicit (⚡, breaks) | Minimal |
| Chunks per section | 3-5 items | 5-7 items |

**Personal story:**

I have ADHD and built v1-v2 exclusively for us. But neurotypical friends wanted to use it too (especially during burnout/stress). v3.0 makes it inclusive while keeping ADHD mode as the compassionate default.

**Backward compatible:** If you're already using v2, nothing changes. v3 defaults to ADHD mode. Neurotypical mode is opt-in.

**Installation:** Same as before
```bash
/plugin install neurodivergent-visual-org@superpowers-marketplace
```

**Repository:** https://github.com/JackReis/neurodivergent-visual-org

Feedback welcome! Built with ADHD, for the community (and allies).

---

## Reddit - r/autism

**Title:** [Tool Update] Visual organization tool now has neurotypical/autistic mode toggle (v3.0)

**Post:**

Update on the visual organization tool I shared for executive dysfunction:

**New in v3.0: Dual Mode System**

You can now toggle between autistic-friendly and neurotypical modes.

**Why this helps:**

**Autistic Mode (Default):**
- Clear, unambiguous language
- Realistic time estimates (no "should only take 5 minutes" lies)
- Explicit structure and scaffolding
- Energy-aware planning
- No NT assumptions about executive function

**Neurotypical Mode:**
- Standard professional format
- For team presentations or work contexts
- Same tool, different audience

**Auto-Detection:**

The tool analyzes your language:
- "I'm overwhelmed" → Autistic mode (compassionate support)
- "Create project plan" → Neurotypical mode (professional format)
- Ambiguous → Defaults to autistic mode (inclusive design)

**Example:**

**Your request:** "I have too many things on my plate and can't figure out what to do first"

**Autistic mode output:**
- Step-by-step triage flowchart
- Concrete criteria for each decision
- Energy cost indicators
- Permission to skip low-priority items
- "It's okay to say no" scaffolding

**Same request, neurotypical mode:**
- Eisenhower matrix (urgent/important)
- Standard prioritization framework
- Professional presentation

**Configuration:**

Set your default in `.claude/neurodivergent-visual-org-preference.yml`:
```yaml
mode: neurodivergent  # or neurotypical, or auto-detect
chunk_size_max: 5
time_buffer_multiplier: 1.5
```

**Inclusive by design:**

- Autistic mode: default (built for us first)
- Neurotypical mode: opt-in (for work contexts)
- Auto-detect: adapts to current needs
- No NT assumptions forced on anyone

**Repository:** https://github.com/JackReis/neurodivergent-visual-org

Free, open source, MIT license.

---

## Twitter/X Thread (7 tweets)

**Tweet 1:**
v3.0 of my ADHD visual organization tool just dropped 🧠✨

New feature: Neurotypical/Neurodivergent mode toggle

Same tool, two modes:
- ADHD mode for personal planning
- NT mode for team presentations

Auto-detects which you need based on your language

Thread ⬇️

**Tweet 2:**
How auto-detect works:

"I'm overwhelmed by this project" → ADHD mode
→ 3-min micro-steps
→ Compassionate language
→ Energy tracking
→ Break reminders

"Create Q4 timeline" → NT mode
→ Standard tasks
→ Professional format

**Tweet 3:**
Mode comparison:

ADHD Mode:
✅ 3-10 min micro-steps
✅ "You've got this!" language
✅ 2x time buffer
✅ Energy indicators (⚡)
✅ 3-5 items per section

NT Mode:
📊 15-30 min tasks
📊 Direct, professional
📊 Standard time estimates
📊 5-7 items per section

**Tweet 4:**
Why I built this:

v1-v2: ADHD-only (because that's what I needed)

v3: Inclusive toggle because:
- NT friends wanted it during burnout
- Work presentations need NT format
- Mixed teams need both modes
- Stress impairs executive function (any neurotype)

**Tweet 5:**
Example use case:

Morning: Use ADHD mode for personal task breakdown
→ Compassionate, micro-steps, energy-aware

Afternoon: Switch to NT mode for team standup
→ Professional, efficient, stakeholder-ready

Same project. Two audiences. One tool.

**Tweet 6:**
Backward compatible:

Using v2? Nothing changes.
v3 defaults to ADHD mode.

NT mode is opt-in:
"Use neurotypical mode"
OR set in config file

Inclusive default = ADHD-friendly 💙

**Tweet 7:**
Try it:
```
/plugin install neurodivergent-visual-org@superpowers-marketplace
```

GitHub: https://github.com/JackReis/neurodivergent-visual-org

Built with ADHD, for the community (and allies)

Free • Open Source • MIT License

---

## LinkedIn (Professional)

**Title:** Building Cognitive Accessibility into AI Tools: v3.0 Release

**Post:**

Excited to share v3.0 of the neurodivergent visual organization tool - now with adaptive mode switching.

**The Problem:**

Traditional productivity tools assume neurotypical executive function. For the 15-20% of people with ADHD, autism, or other neurodivergent conditions, these tools often increase overwhelm rather than reduce it.

**The Solution (v1-v2):**

Visual diagrams optimized for neurodivergent cognition:
- Working memory limits: 3-5 chunks (ADHD) vs 5-7 (neurotypical)
- Time perception: 1.5-2x buffers for realistic planning
- Energy awareness: Cognitive load tracking
- Compassionate design: Anti-perfectionism, permission statements

**The Evolution (v3.0):**

Added neurotypical/neurodivergent mode toggle based on user feedback:

**Use Cases:**
1. **Personal planning** - ADHD mode for executive function support
2. **Professional presentations** - Neurotypical mode for stakeholders
3. **Mixed teams** - Auto-detect adapts to each person
4. **Stress/burnout** - Even neurotypical users benefit from supportive mode

**Technical Implementation:**

- Dual template system (separate pattern libraries per mode)
- Auto-detection via natural language analysis
- User configuration for default preferences
- Backward compatible (defaults to neurodivergent mode)

**Impact:**

This addresses a critical gap in accessibility tooling. Cognitive diversity is often overlooked in product design, yet affects communication, productivity, and team dynamics significantly.

**Design Principle:**

"Inclusive by default, adaptable by choice"

- Neurodivergent mode: default (built for the underserved community)
- Neurotypical mode: opt-in (for specific contexts)
- Auto-detect: intelligent adaptation

**Open Source:**

MIT License - Available in Claude Code superpowers marketplace

GitHub: https://github.com/JackReis/neurodivergent-visual-org

**Looking Forward:**

Cognitive accessibility in AI tools is still emerging. Would love to connect with others working on neurodiversity inclusion, adaptive interfaces, or accessibility-first product design.

#Neurodiversity #Accessibility #ADHD #Autism #ProductDesign #AI #OpenSource #CognitiveAccessibility #InclusiveDesign

---

## Blog Post Outline (Medium/Dev.to)

**Title:** Building Adaptive Cognitive Modes: Lessons from v3.0

**Sections:**

1. **The Journey So Far**
   - v1: Basic ADHD-friendly patterns
   - v2: Research-backed design (neuroscience, cognitive load theory)
   - v3: Adaptive mode system

2. **Why Mode Switching Matters**
   - Personal story: ADHD mode for me, NT mode for presentations
   - User feedback: "Can my neurotypical team use this?"
   - Insight: Stress impairs executive function across neurotypes

3. **Technical Design: Dual Template System**
   - Separate pattern libraries per mode
   - Mode detection algorithm
   - Configuration system
   - Backward compatibility strategy

4. **Mode Characteristics Deep Dive**
   - Chunk size: Miller's Law (7±2) vs ADHD adaptation (3-5)
   - Time estimation: Buffer psychology
   - Language design: Compassion vs efficiency
   - Color psychology: Calming vs standard

5. **Auto-Detection Logic**
   - Distress signal keywords
   - Neurodivergent condition mentions
   - Energy-aware language
   - Professional context detection
   - Default to inclusive (neurodivergent mode)

6. **Real-World Use Cases**
   - Solo ADHD user: Personal planning
   - Mixed team: Adaptive per person
   - Neurotypical during burnout: Stress support
   - Professional presentations: Mode switching

7. **Lessons Learned**
   - Build for underserved community first
   - Inclusivity doesn't mean "one size fits all"
   - Auto-detection reduces friction
   - Configuration enables power users
   - Backward compatibility is non-negotiable

8. **What's Next**
   - v4 ideas: Custom modes, team templates, integration APIs
   - Community feedback loop
   - Cognitive accessibility as a field

**Call to Action:**
- Try the tool: Installation instructions
- Contribute: GitHub repo
- Connect: LinkedIn for cognitive accessibility discussions

---

## Usage Tips for v3.0 Posts

**Key Messages:**

1. **Inclusive design** - Built for neurodivergent, adaptable for all
2. **Mode toggle** - Same tool, different cognitive styles
3. **Auto-detection** - Intelligent adaptation to user needs
4. **Backward compatible** - Existing users unaffected
5. **Open source** - MIT license, community-driven

**Positioning:**

- v1-v2: "Built for neurodivergent community"
- v3: "Built WITH neurodivergent community, now accessible to all"

**Avoid:**

- Framing NT mode as "better" or "standard"
- Suggesting neurodivergent mode is "simplified" (it's optimized, not dumbed-down)
- Implying neurotypical users are the primary audience

**Emphasize:**

- Neurodivergent mode is the default (inclusive first principle)
- NT users benefit during stress/burnout (universal design)
- Mode choice respects user agency
- Tool works WITH brain differences, not against them
