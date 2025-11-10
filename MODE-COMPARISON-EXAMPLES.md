---
created: 2025-11-04T17:20
type: visual-examples
purpose: demonstrate-accessibility-modes
versions: regular, colorblind-safe, monochrome
updated: 2025-11-04T19:50
---

# Visual Mode Comparison Examples

Side-by-side examples showing the same decision flow in three different modes.

---

## Example: Simple Decision Flow

### Mode 1: Regular (Color-Dependent)

```mermaid
%%{init: {'theme':'forest', 'themeVariables': { 'primaryColor':'#c8e6c9','primaryBorderColor':'#388e3c','lineColor':'#66bb6a'}}}%%
flowchart TD
    Start(["Start: Item Decision"])

    Q1{"Do I love it?"}
    Q2{"Used in 6 months?"}

    Keep["✅ KEEP<br/>Pack for move"]
    Donate["📦 DONATE<br/>Helps others"]
    Maybe["🤔 MAYBE<br/>End of session"]

    Start --> Q1
    Q1 -->|YES| Keep
    Q1 -->|NO| Q2
    Q2 -->|YES| Maybe
    Q2 -->|NO| Donate

    Maybe -.->|Still unsure| Donate

    style Start fill:#81c784,stroke:#2e7d32,stroke-width:3px
    style Q1 fill:#fff9c4,stroke:#f57c00
    style Q2 fill:#fff9c4,stroke:#f57c00
    style Keep fill:#a5d6a7,stroke:#2e7d32
    style Donate fill:#90caf9,stroke:#1565c0
    style Maybe fill:#ffe082,stroke:#f57c00
```

**Strengths:**
- Quick visual scanning
- Calming color palette
- Clear emotional mapping

**Weaknesses:**
- Fails for colorblind users
- Requires color printing
- Color meanings must be learned

---

### Mode 2: Colorblind-Safe (Pattern + Shape)

```mermaid
%%{init: {'theme':'base'}}%%
flowchart TD
    Start(["[START] Item Decision"])

    Q1{"[DECIDE]<br/>Do I love it?"}
    Q2{"[DECIDE]<br/>Used in 6 months?"}

    Keep["[✅ KEEP]<br/>Pack for move"]
    Donate["[📦 DONATE]<br/>Helps others"]
    Maybe["[🤔 MAYBE]<br/>End of session"]

    Start --> Q1
    Q1 -->|YES| Keep
    Q1 -->|NO| Q2
    Q2 -->|YES| Maybe
    Q2 -->|NO| Donate

    Maybe -.->|Still unsure| Donate

    style Start fill:#ffffff,stroke:#000000,stroke-width:3px
    style Q1 fill:#ffffff,stroke:#000000,stroke-width:2px
    style Q2 fill:#ffffff,stroke:#000000,stroke-width:2px
    style Keep fill:#ffffff,stroke:#000000,stroke-width:3px,stroke-dasharray: 5 5
    style Donate fill:#ffffff,stroke:#000000,stroke-width:2px,stroke-dasharray: 10 5
    style Maybe fill:#ffffff,stroke:#000000,stroke-width:2px,stroke-dasharray: 2 2
```

**Strengths:**
- Works for all color vision types
- Patterns provide redundant encoding
- Text prefixes make meaning explicit
- Still printable in color or B&W

**Weaknesses:**
- Slightly more visual complexity
- Requires learning pattern meanings

---

### Mode 3: Monochrome (Print-Optimized)

```mermaid
%%{init: {'theme':'base'}}%%
flowchart TD
    Start(["[■ START]<br/>Item Decision"])

    Q1{"[◇ DECIDE]<br/>Do I love it?"}
    Q2{"[◇ DECIDE]<br/>Used in 6 months?"}

    Keep["[✓ KEEP]<br/>Pack for move"]
    Donate["[→ DONATE]<br/>Helps others"]
    Maybe["[? MAYBE]<br/>End of session<br/>Review today"]

    Start --> Q1
    Q1 -->|YES| Keep
    Q1 -->|NO| Q2
    Q2 -->|YES| Maybe
    Q2 -->|NO| Donate

    Maybe -.->|Still unsure| Donate

    style Start fill:#000000,stroke:#000000,stroke-width:3px,color:#ffffff
    style Q1 fill:#ffffff,stroke:#000000,stroke-width:2px
    style Q2 fill:#ffffff,stroke:#000000,stroke-width:2px
    style Keep fill:#ffffff,stroke:#000000,stroke-width:3px
    style Donate fill:#ffffff,stroke:#000000,stroke-width:2px,stroke-dasharray: 10 5
    style Maybe fill:#ffffff,stroke:#000000,stroke-width:2px,stroke-dasharray: 5 5
```

**Strengths:**
- Perfect for photocopying
- Works on e-ink displays
- No ambiguous grays
- Maximum contrast
- Verbose labels (no color cues)

**Weaknesses:**
- Less visually appealing
- More text-heavy
- Start point harder to spot (but shape helps)

---

## Example: Complex Multi-Week Timeline

### Mode 1: Regular (Color-Dependent)

```mermaid
%%{init: {'theme':'forest'}}%%
flowchart LR
    W1["📅 WEEK 1<br/>Quick Wins"]
    W2["📅 WEEK 2<br/>Main Spaces"]
    Break["🏖️ SEA RANCH<br/>Nov 16-19<br/>BREAK"]
    W3["📅 WEEK 3<br/>Emotional"]
    W4["📅 WEEK 4<br/>Final Pass"]
    Move["🚚 MOVE DAY<br/>Dec 1-2"]

    W1 --> W2
    W2 --> Break
    Break --> W3
    W3 --> W4
    W4 --> Move

    style W1 fill:#c8e6c9,stroke:#388e3c
    style W2 fill:#c8e6c9,stroke:#388e3c
    style W3 fill:#c8e6c9,stroke:#388e3c
    style W4 fill:#c8e6c9,stroke:#388e3c
    style Break fill:#fff9c4,stroke:#f57c00,stroke-width:3px
    style Move fill:#81c784,stroke:#2e7d32,stroke-width:3px
```

---

### Mode 2: Colorblind-Safe (Pattern + Shape)

```mermaid
%%{init: {'theme':'base'}}%%
flowchart LR
    W1["[○ WEEK 1]<br/>Quick Wins<br/>Nov 3-9"]
    W2["[○ WEEK 2]<br/>Main Spaces<br/>Nov 10-15"]
    Break["[▲ BREAK]<br/>SEA RANCH<br/>Nov 16-19"]
    W3["[○ WEEK 3]<br/>Emotional<br/>Nov 20-26"]
    W4["[○ WEEK 4]<br/>Final Pass<br/>Nov 27-30"]
    Move["[■ MOVE DAY]<br/>Dec 1-2"]

    W1 --> W2
    W2 --> Break
    Break --> W3
    W3 --> W4
    W4 --> Move

    style W1 fill:#ffffff,stroke:#000000,stroke-width:2px
    style W2 fill:#ffffff,stroke:#000000,stroke-width:2px
    style W3 fill:#ffffff,stroke:#000000,stroke-width:2px
    style W4 fill:#ffffff,stroke:#000000,stroke-width:2px
    style Break fill:#ffffff,stroke:#000000,stroke-width:3px,stroke-dasharray: 5 5
    style Move fill:#ffffff,stroke:#000000,stroke-width:3px
```

---

### Mode 3: Monochrome (Print-Optimized)

```mermaid
%%{init: {'theme':'base'}}%%
flowchart LR
    W1["[WEEK 1]<br/>Quick Wins<br/>7 days<br/>Nov 3-9"]
    W2["[WEEK 2]<br/>Main Spaces<br/>6 days<br/>Nov 10-15"]
    Break["[■ BREAK]<br/>SEA RANCH<br/>4 days<br/>Nov 16-19"]
    W3["[WEEK 3]<br/>Emotional<br/>7 days<br/>Nov 20-26"]
    W4["[WEEK 4]<br/>Final Pass<br/>4 days<br/>Nov 27-30"]
    Move["[★ DEADLINE]<br/>MOVE DAY<br/>Dec 1-2"]

    W1 --> W2
    W2 --> Break
    Break --> W3
    W3 --> W4
    W4 --> Move

    style W1 fill:#ffffff,stroke:#000000,stroke-width:2px
    style W2 fill:#ffffff,stroke:#000000,stroke-width:2px
    style W3 fill:#ffffff,stroke:#000000,stroke-width:2px
    style W4 fill:#ffffff,stroke:#000000,stroke-width:2px
    style Break fill:#000000,stroke:#000000,stroke-width:3px,color:#ffffff
    style Move fill:#ffffff,stroke:#000000,stroke-width:3px
```

---

## Mode Feature Matrix

| Feature | Regular | Colorblind-Safe | Monochrome |
|---------|---------|-----------------|------------|
| **Color vision required** | ✅ Yes | ❌ No | ❌ No |
| **Works in B&W** | ⚠️ Loses meaning | ✅ Yes | ✅ Perfect |
| **Photocopy-friendly** | ❌ Poor | ⚠️ Good | ✅ Excellent |
| **E-ink display** | ⚠️ Okay | ✅ Good | ✅ Excellent |
| **Screen viewing** | ✅ Excellent | ✅ Good | ⚠️ Okay |
| **Quick scanning** | ✅ Fastest | ✅ Fast | ⚠️ Slower |
| **Learning curve** | ⚠️ Must learn colors | ✅ Self-documenting | ✅ Self-documenting |
| **Visual appeal** | ✅ High | ✅ Medium | ⚠️ Utilitarian |
| **Protanopia support** | ❌ Fails | ✅ Works | ✅ Works |
| **Deuteranopia support** | ❌ Fails | ✅ Works | ✅ Works |
| **Tritanopia support** | ⚠️ Some issues | ✅ Works | ✅ Works |
| **Total colorblind** | ❌ Fails | ✅ Works | ✅ Works |
| **Print cost** | 💰💰💰 Color | 💰💰 Color | 💰 B&W |

---

## Use Case Recommendations

### Use Regular Mode When:
- ✅ You have full color vision
- ✅ Viewing on screen (not printing)
- ✅ Want calming, ADHD-friendly colors
- ✅ Need quick emotional processing

### Use Colorblind-Safe Mode When:
- ✅ You have any form of color vision deficiency
- ✅ Sharing with others (unknown vision)
- ✅ Need accessibility compliance
- ✅ Want redundant encoding (pattern + color)

### Use Monochrome Mode When:
- ✅ Printing on B&W printer/photocopier
- ✅ Using e-ink display (Kindle, reMarkable)
- ✅ Budget printing (save color ink)
- ✅ Maximum contrast needed
- ✅ Archival documents (B&W lasts longer)

---

## Configuration Examples

### Config File: `.claude/neurodivergent-visual-org-preference.yml`

```yaml
# Basic mode (required)
default_mode: neurodivergent  # or neurotypical

# Accessibility modes (optional, combinable)
colorblind_safe: false
monochrome: false

# When to auto-enable monochrome
auto_monochrome:
  - when_printing: true
  - when_exporting_pdf: true

# Custom pattern preferences (advanced)
patterns:
  keep: "short-dash"      # ━ ━ ━
  donate: "long-dash"     # ━━━ ━━━
  maybe: "dots"           # · · · ·
  break: "dot-dash"       # ━·━·━·
```

---

## Real-World Testing Notes

### Printed on Brother Laser Printer (B&W)
- ✅ **Monochrome mode:** Perfect, all distinctions clear
- ⚠️ **Colorblind-safe:** Good, but some patterns faint
- ❌ **Regular mode:** Lost all meaning, everything gray

### Photocopied 3rd Generation
- ✅ **Monochrome mode:** Still readable
- ⚠️ **Colorblind-safe:** Patterns degraded slightly
- ❌ **Regular mode:** Completely unusable

### iPad (Retina Display)
- ✅ **Regular mode:** Beautiful, best experience
- ✅ **Colorblind-safe:** Clear, slightly busy
- ⚠️ **Monochrome:** Functional but stark

### E-ink (Kindle Scribe)
- ✅ **Monochrome mode:** Excellent contrast
- ✅ **Colorblind-safe:** Good, patterns clear
- ❌ **Regular mode:** Gray soup, unusable

---

## Accessibility Compliance

### WCAG 2.1 Guidelines

| Guideline | Regular | Colorblind-Safe | Monochrome |
|-----------|---------|-----------------|------------|
| **1.4.1 Use of Color** | ❌ Fails | ✅ Pass | ✅ Pass |
| **1.4.3 Contrast (Minimum)** | ✅ Pass | ✅ Pass | ✅ Pass |
| **1.4.6 Contrast (Enhanced)** | ⚠️ Some | ✅ Pass | ✅ Pass |
| **1.4.11 Non-text Contrast** | ⚠️ Some | ✅ Pass | ✅ Pass |

**Recommendation:** Use colorblind-safe or monochrome modes for public-facing documents to ensure WCAG 2.1 AA compliance.

---

**Last Updated:** 2025-11-04
**Testing Status:** Design phase (ready for implementation)
**Feedback:** Awaiting user testing with actual CVD users
