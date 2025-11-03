---
mode: neurotypical
template: decision-tree
---
# Neurotypical Decision Tree Templates

## Binary Decision Tree

```mermaid
flowchart TD
    Question([Decision Point]) --> Factor1{Primary Factor?}
    Factor1 -->|Yes| Factor2{Secondary Factor?}
    Factor1 -->|No| OptionB[Option B]
    Factor2 -->|Yes| OptionA1[Option A - Variant 1]
    Factor2 -->|No| OptionA2[Option A - Variant 2]

    style Question fill:#d4e6f1
    style OptionA1 fill:#d5f4e6
    style OptionA2 fill:#d5f4e6
    style OptionB fill:#fdecea
```

## Weighted Decision Matrix

```mermaid
quadrantChart
    title Decision Matrix: Options Evaluation
    x-axis Low Effort --> High Effort
    y-axis Low Impact --> High Impact
    quadrant-1 High Priority
    quadrant-2 Strategic Investment
    quadrant-3 Low Priority
    quadrant-4 Quick Wins

    Option A: [0.3, 0.8]
    Option B: [0.7, 0.7]
    Option C: [0.2, 0.3]
    Option D: [0.8, 0.4]
```

**Characteristics:**
- Standard decision theory approach
- Efficient visual layout
- Professional color schemes
- Assumes rational decision-making process
