---
mode: neurotypical
template: decision-tree
created: 2025-11-03T00:25
updated: 2025-11-04T13:21
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

[🎨 Edit Flowchart in mermaid.live](https://mermaid.live/edit#flowchart%20TD%0A%20%20%20%20Question%28%5BDecision%20Point%5D%29%20--%3E%20Factor1%7BPrimary%20Factor%3F%7D%0A%20%20%20%20Factor1%20--%3E%7CYes%7C%20Factor2%7BSecondary%20Factor%3F%7D%0A%20%20%20%20Factor1%20--%3E%7CNo%7C%20OptionB%5BOption%20B%5D%0A%20%20%20%20Factor2%20--%3E%7CYes%7C%20OptionA1%5BOption%20A%20-%20Variant%201%5D%0A%20%20%20%20Factor2%20--%3E%7CNo%7C%20OptionA2%5BOption%20A%20-%20Variant%202%5D%0A%0A%20%20%20%20style%20Question%20fill%3A%23d4e6f1%0A%20%20%20%20style%20OptionA1%20fill%3A%23d5f4e6%0A%20%20%20%20style%20OptionA2%20fill%3A%23d5f4e6%0A%20%20%20%20style%20OptionB%20fill%3A%23fdecea%0A)


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

[🎨 Edit Diagram in mermaid.live](https://mermaid.live/edit#quadrantChart%0A%20%20%20%20title%20Decision%20Matrix%3A%20Options%20Evaluation%0A%20%20%20%20x-axis%20Low%20Effort%20--%3E%20High%20Effort%0A%20%20%20%20y-axis%20Low%20Impact%20--%3E%20High%20Impact%0A%20%20%20%20quadrant-1%20High%20Priority%0A%20%20%20%20quadrant-2%20Strategic%20Investment%0A%20%20%20%20quadrant-3%20Low%20Priority%0A%20%20%20%20quadrant-4%20Quick%20Wins%0A%0A%20%20%20%20Option%20A%3A%20%5B0.3%2C%200.8%5D%0A%20%20%20%20Option%20B%3A%20%5B0.7%2C%200.7%5D%0A%20%20%20%20Option%20C%3A%20%5B0.2%2C%200.3%5D%0A%20%20%20%20Option%20D%3A%20%5B0.8%2C%200.4%5D%0A)


**Characteristics:**
- Standard decision theory approach
- Efficient visual layout
- Professional color schemes
- Assumes rational decision-making process
