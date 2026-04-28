#### [🏠 Table of Contents](./README.md)

###### [⬅️ Chapter 3: Engineering the System Prompt](./chapter-3.md)

---

# Chapter 4: The Art of Framing (The Input Interface)

> While the system prompt sets the overall "firmware," the individual prompt is the "instruction set" for a specific task. If the individual prompt is framed poorly, it can override the system prompt and re-trigger the Critic's obsessive loops.

The goal of framing is to provide the model with a narrow, well-defined search space. The more ambiguity there is in a prompt, the more room the Critic has to find "flaws" and initiate a reasoning loop.

## 4.1 The Superlative Trap
The "Superlative Trap" occurs when a user asks for the "best," "most optimal," or "perfect" solution. Because "optimal" is subjective and multi-dimensional (e.g., optimal for speed? for memory? for readability?), the Critic is forced to evaluate every possible dimension simultaneously.

### Transitioning to Objective Metrics
To avoid this, replace subjective superlatives with objective, measurable constraints.

*   **❌ Superlative:** "Write the **most optimal** sorting algorithm for this data."
*   **✅ Objective:** "Write a sorting algorithm that prioritizes **minimal memory overhead** (O(1) space) and accepts a slower time complexity."

By specifying the metric (memory overhead), you tell the Critic exactly what to validate, allowing it to ignore other dimensions (like raw speed) that would otherwise trigger a loop.

## 4.2 Defining the Trade-off (Limiting the Search Space)
In software engineering, every architectural choice is a trade-off. If a prompt asks for a high-performance solution without specifying the "cost" the user is willing to pay, the model will attempt to find a "zero-cost" solution—which does not exist. This pursuit of the impossible is a primary driver of infinite reasoning loops.

To prevent this, explicitly define the trade-off.

**Common Trade-off Pairs:**
*   **Latency vs. Throughput:** "Prioritize low per-request latency over total system throughput."
*   **Memory vs. CPU:** "Prioritize minimal RAM usage; I am willing to accept higher CPU utilization for decompression."
*   **Readability vs. Performance:** "Prioritize maintainability and clean abstraction over micro-optimizations."

By defining the trade-off, you effectively "wall off" parts of the search space, giving the Critic a clear boundary of what is acceptable and what is not.

## 4.3 Objective Constraints vs. Subjective Goals
Subjective goals provide "Critic bait"—they are open to interpretation and therefore open to endless debate. Objective constraints provide "Generator instructions"—they are binary (either the condition is met, or it isn't).

### Comparison Table: Subjective vs. Objective

| Subjective Goal (Avoid) | Objective Constraint (Use) | Result |
| :--- | :--- | :--- |
| "Make the code clean." | "Follow the Google C++ Style Guide." | Replaces "opinion" with a "standard." |
| "Ensure it's robust." | "Handle null pointers and out-of-bounds access." | Replaces "feeling" with "specific cases." |
| "Use an advanced pattern." | "Implement this using the Strategy Pattern." | Replaces "vague" with "concrete." |
| "Make it fast." | "The execution time must be under 10ms." | Replaces "relative" with "absolute." |

## 4.4 Summary for the Operator
When framing a prompt, ask yourself: *"Am I asking for a quality (subjective) or a specification (objective)?"*

**The Golden Rule of Framing:**
The more you constrain the model, the more stable the model becomes. Constraints are not limitations; they are the guardrails that prevent the Critic from spiraling into an infinite loop.

---

###### [🏠 Table of Contents](./README.md)
###### [⬅️ Introduction: The Shift in Perspective](./intro.md)
###### [⬅️ Chapter 1: The Architecture of Thought](./chapter-1.md)
###### [⬅️ Chapter 2: Linguistic Tuning (The Vocabulary of Control)](./chapter-2.md)
###### [⬅️ Chapter 3: Engineering the System Prompt](./chapter-3.md)

- [x] Chapter 4

### [➡️ Chapter 5: Workflow Optimization (The Process)](./chapter-5.md)
###### [➡️ Chapter 6: Real-Time Supervision (Course Correction)](./chapter-6.md)
###### [➡️ Chapter 7: Quick Reference & Cheat Sheets](./chapter-7.md)
###### [➡️ Appendix: Technical Lexicon](./appendix.md)
