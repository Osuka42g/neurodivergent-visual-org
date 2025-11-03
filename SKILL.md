---
name: neurodivergent-visual-org
description: Create visual organizational tools (mind maps, task breakdowns, decision trees, kanban boards, project timelines) designed for neurodivergent thinking patterns. Use when users feel overwhelmed, need to break down tasks, navigate decisions, see dependencies, or track current state. Emphasizes compassionate language, realistic time estimates, energy-aware planning, and anti-perfectionism.
created: 2025-11-02T21:50
updated: 2025-11-02T21:51
---

# Neurodivergent Visual Organization

Create visual organizational tools that make invisible work visible and reduce cognitive overwhelm. This skill generates Mermaid diagrams optimized for neurodivergent thinking patterns.

## When to Use This Skill

Use when the user:
- Feels overwhelmed by a task or project ("I don't know where to start")
- Needs to break down something complex into steps
- Is stuck making a decision or mentions analysis paralysis
- Asks "what should I focus on?" or "what's on my plate?"
- Mentions executive dysfunction, time blindness, or decision fatigue
- Wants to see how tasks connect or depend on each other
- Needs to track progress across multiple things
- Says something feels "too big" or "too much"

## Core Principles

**Always apply these principles:**
- Use compassionate, non-judgmental language
- Give realistic time estimates with buffer (not "should only take")
- Acknowledge energy costs, not just time
- Break tasks into 3-10 minute micro-steps
- Include "you can modify this" permission statements
- Celebrate starting, not just finishing
- Make "done" concrete and achievable
- Show progress, not just what's left

## Quick Selection Guide

Choose the right visualization type:

| User Need | Visualization Type | Reference File |
|-----------|-------------------|----------------|
| "I don't know where to start" | Task breakdown timeline | task-breakdowns.md |
| "This task is overwhelming" | Linear or branching breakdown | task-breakdowns.md |
| "I'm stuck between options" | Decision tree or matrix | decision-tools.md |
| "I can't decide" | Elimination or weighted decision | decision-tools.md |
| "What should I focus on?" | Priority matrix or current state | current-state-boards.md |
| "I have too many things" | Kanban board or triage flow | current-state-boards.md |
| "How do I do this project?" | Project phases or dependency map | project-maps.md |
| "This project feels huge" | MVP breakdown or phases | project-maps.md |
| "I can't focus" or "Need to start work" | Pre-task prep or Pomodoro | time-boxing.md |
| "Struggling with time blindness" | Time-blocked day or energy mapping | time-boxing.md |
| "Want to build a habit" | Tiny habit builder or stacking | habit-building.md |
| "Morning/evening routine help" | Routine sequence or wind-down | habit-building.md |
| "Need accountability" | Body doubling or check-in schedule | accountability-support.md |
| "When should I ask for help?" | Reach-out decision tree | accountability-support.md |
| "Can't settle to work" | Regulation protocol or sensory toolkit | focus-regulation.md |
| "Crashed after hyperfocus" | Recovery protocol | focus-regulation.md |

## Workflow

### Step 1: Understand the Need

Ask clarifying questions if needed:
- What specifically feels overwhelming?
- What's the desired outcome?
- What's the time frame (if any)?
- What's your current energy level?

### Step 2: Select Pattern

Based on the user's need, select the appropriate pattern from the reference files:
- **references/task-breakdowns.md** - Linear timelines, branching breakdowns, energy-aware sequences
- **references/decision-tools.md** - Decision trees, weighted matrices, elimination filters
- **references/project-maps.md** - Phase maps, dependency diagrams, MVP breakdowns
- **references/current-state-boards.md** - Kanban boards, priority matrices, context tracking
- **references/time-boxing.md** - Pomodoro technique, time-blocked days, focus sessions, energy mapping
- **references/habit-building.md** - Tiny habits, routine sequences, habit stacking, momentum tracking
- **references/accountability-support.md** - Body doubling, check-ins, support networks, crisis protocols
- **references/focus-regulation.md** - Pre-task calm-down, sensory tools, emotional regulation, recovery

Read the relevant reference file to see specific patterns and examples.

### Step 3: Generate Visualization

Create a Mermaid diagram following the pattern. Customize it with:
- User's specific tasks/options/context
- Realistic time estimates (be generous)
- Energy indicators (⚡ symbols)
- Compassionate language
- Clear next actions

Use the Mermaid validation tool to render the diagram.

### Step 4: Provide Context

After showing the diagram, include:
- Brief explanation of how to use it
- Permission statements ("you can modify this")
- Encouragement ("starting is the hardest part")
- Offer to save to Obsidian vault if relevant

## Using Reference Files

**Always read the relevant reference file before generating a visualization** to see proven patterns and examples.

The reference files contain:
- **Specific Mermaid patterns** that work well
- **Example diagrams** you can adapt
- **Language guidelines** for neurodivergent-friendly phrasing
- **When to use** each pattern type

Don't reinvent patterns - use the proven examples in the references and customize them to the user's specific situation.

## Integration with Obsidian

If the user wants to save visualizations:
1. Use the `obsidian:create` tool to create a new note
2. Include the Mermaid code block in the note
3. Add context/instructions above the diagram
4. Use a clear filename (e.g., "Project Breakdown - Home Office.md")

## Anti-Patterns to Avoid

❌ Don't create overwhelming diagrams with too many nodes
❌ Don't use judgmental language ("just do it", "should be easy")
❌ Don't set unrealistic time estimates
❌ Don't create diagrams without context/instructions
❌ Don't forget to acknowledge energy costs
❌ Don't make everything urgent/high-priority

## Example Usage

**User:** "I need to clean my apartment but it's so messy I don't know where to start"

**Claude:** Reads task-breakdowns.md, selects "Linear Task Timeline" pattern, generates a Gantt chart breaking "clean apartment" into 15-minute phases starting with "quick wins" (grab trash, collect dishes), includes time estimates, uses encouraging language, renders with Mermaid tool.

**User:** "Should I take this new job offer or stay at my current job?"

**Claude:** Reads decision-tools.md, asks about key factors that matter to them, creates a weighted decision matrix showing both options scored across their priorities, includes reflection prompt about tradeoffs, renders diagram.

**User:** "I have too many things on my plate and can't figure out what to do first"

**Claude:** Reads current-state-boards.md, selects "Too Many Things Triage" pattern, creates a flowchart that helps them sort tasks into "truly urgent", "important", "maybe later", and "need clarity", includes compassionate language, shows next actions.
