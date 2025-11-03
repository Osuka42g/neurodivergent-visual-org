---
created: 2025-11-02
updated: 2025-11-03T00:30
---
# Mode Comparison Examples

## Example 1: Apartment Cleaning Task

### User Request
"I need to clean my apartment but it's so messy I don't know where to start"

**Auto-Detect Result:** Neurodivergent mode (keywords: "so messy", "don't know where to start")

### Neurodivergent Mode Output

```mermaid
gantt
    title Apartment Cleaning - 15 Min Phases (You've Got This!)
    dateFormat HH:mm
    axisFormat %H:%M

    section Quick Wins (Start Here!)
    Grab visible trash + cups (3 min) ⚡  :milestone, 09:00, 3m
    Collect dishes to kitchen (5 min)     :09:03, 5m
    ☕ Break - You deserve it!             :milestone, 09:08, 0m

    section Kitchen (Medium Energy ⚡⚡)
    Load dishwasher (8 min)               :09:08, 8m
    Wipe counters (5 min)                 :09:16, 5m
    ☕ Break if needed                     :milestone, 09:21, 0m

    section Living Room (You're doing great!)
    Clear coffee table (7 min)            :09:21, 7m
    Vacuum main area (10 min)             :09:28, 10m

    section Bedroom (Optional - stop if tired!)
    Make bed (3 min)                      :09:38, 3m
```

**Language:** "You've Got This!", "You deserve it!", "You're doing great!", "Optional - stop if tired!"

**Time estimates:** 3-10 minute micro-steps with breaks

**Energy indicators:** ⚡ symbols, explicit break points

**Permission:** "Optional", "if needed", "stop if tired"

### Neurotypical Mode Output

```mermaid
gantt
    title Apartment Cleaning - Efficient Breakdown
    dateFormat HH:mm
    axisFormat %H:%M

    section Kitchen
    Clear dishes and load dishwasher  :09:00, 15m
    Wipe surfaces                     :09:15, 10m

    section Living Areas
    Clear clutter and organize        :09:25, 20m
    Vacuum all rooms                  :09:45, 15m

    section Bedroom
    Make bed and organize             :10:00, 15m

    section Bathroom
    Quick clean                       :10:15, 15m
```

**Language:** Direct, task-focused

**Time estimates:** 15-20 minute tasks, standard duration

**Energy indicators:** None (assumes sustained focus)

**Permission:** None (assumes self-directed execution)

---

## Example 2: Career Decision

### User Request
"Should I take this new job offer or stay at my current job?"

**Auto-Detect Result:** Neurotypical mode (no distress signals, straightforward decision request)

### Neurotypical Mode Output

```mermaid
quadrantChart
    title Job Decision Matrix
    x-axis Low Satisfaction --> High Satisfaction
    y-axis Low Growth --> High Growth
    quadrant-1 Pursue Aggressively
    quadrant-2 Strategic Investment
    quadrant-3 Reconsider
    quadrant-4 Golden Handcuffs

    Current Job: [0.6, 0.4]
    New Offer: [0.7, 0.8]
```

**Factors to evaluate:**
1. Salary and compensation
2. Growth opportunities
3. Work-life balance
4. Team and culture fit
5. Career trajectory
6. Location and commute

**Recommendation:** Score each factor 1-10 for both options, weight by importance, calculate total.

### Neurodivergent Mode Output (if requested)

```mermaid
flowchart TD
    Start([Job Decision - Take Your Time!]) --> Urgent{Is there a deadline?}

    Urgent -->|Yes - Offer expires soon| QuickAnalysis[Quick gut-check analysis]
    Urgent -->|No - I have time| DeepAnalysis[Detailed pros/cons list]

    QuickAnalysis --> GutFeel{What's my gut feeling?}
    GutFeel -->|Excited, energized| Positive[Lean toward new offer]
    GutFeel -->|Anxious, uncertain| Cautious[Consider staying]
    GutFeel -->|Neutral| NeedMore[I need more info]

    DeepAnalysis --> EnergyCheck[How would each affect my daily energy?]
    EnergyCheck --> Current["Current job: <br/>- Known routines ✓<br/>- Established relationships ✓<br/>- Predictable stress levels"]
    EnergyCheck --> New["New offer:<br/>- Learning curve (energy cost!)<br/>- New people (social energy)<br/>- Unknown stress factors"]

    Current --> Values{What matters most to me RIGHT NOW?}
    New --> Values
    NeedMore --> Values

    Values -->|Stability & predictability| StayLean[Leaning toward staying]
    Values -->|Growth & challenge| NewLean[Leaning toward new offer]
    Values -->|Money & benefits| Numbers[Compare actual numbers]

    Positive -.->|Double-check| Values
    Cautious -.->|Double-check| Values

    Numbers --> Decision{Enough information?}
    StayLean --> Decision
    NewLean --> Decision

    Decision -->|Yes| Choose[Make choice - trust yourself!]
    Decision -->|No| Talk[Talk to someone I trust]

    Talk --> Choose

    Choose --> End([Either choice is valid - you've got this!])

    style Start fill:#e1f5e1
    style End fill:#e1f5e1
    style Choose fill:#fff4e6
```

**Language:** "Take Your Time!", "Trust yourself!", "Either choice is valid"

**Energy awareness:** Explicit energy cost analysis for transitions

**Permission:** Multiple valid paths, acknowledges uncertainty is okay

**Scaffolding:** Includes "talk to someone I trust" step

---

## Example 3: Mode Switching Mid-Conversation

### Initial Request (Auto-Detect → Neurodivergent)
User: "I'm overwhelmed by this project and don't know where to start"

*Claude generates neurodivergent mode diagram with micro-steps, compassionate language, energy indicators*

### User Requests Switch
User: "This is great for me, but can you also make a neurotypical version for my team presentation?"

### Response
"Absolutely! I'll create a neurotypical mode version optimized for team presentation. This will be more compact, use standard time estimates, and professional language suitable for stakeholders.

Here's the neurotypical mode version..."

*Claude generates neurotypical mode diagram: efficient, professional, standard granularity*

"**What changed:**
- Task granularity: 3-10 min → 15-30 min tasks
- Language: Compassionate → Direct and professional
- Time estimates: Buffer removed (1.5x → 1.0x)
- Energy scaffolding: Removed (assumes team has executive function)
- Color scheme: Calming → Standard professional

**You now have:**
1. Neurodivergent version for your personal planning
2. Neurotypical version for team presentation

Both represent the same project - just optimized for different audiences!"
```
