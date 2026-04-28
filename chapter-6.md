#### [🏠 Table of Contents](./README.md)

###### [⬅️ Chapter 5: Workflow Optimization (The Process)](./chapter-5.md)

---

# Chapter 6: Real-Time Supervision (Course Correction)

> This chapter assumes that the operator has access to the reasoning trace (the "thought" block) of the model. The goal is to transform the operator from a passive receiver of output into an active **External Supervisor** who can intervene before a reasoning spiral consumes the session.

Despite optimal system prompts and framing, reasoning models can still enter a recursive loop. When this happens, the model is no longer solving the problem; it is solving the *conflict* between its Generator and Critic modules. The operator must intervene to break this cycle.

## 6.1 Identifying the Spiral: Recognition Patterns
The first step in recovery is recognizing the "Spiral" as it happens in the reasoning trace. You do not need to wait for the final output to know the model has failed; the signs are visible in the internal monologue.

**Visual Cues of a Spiral:**
*   **The Pivot Word:** The appearance of words like *"Actually..."*, *"Wait..."*, *"On second thought..."*, or *"Hold on..."*
*   **The Recursive Restart:** The model summarizes the problem again, despite having already established a plan.
*   **The Micro-Obsession:** The model spends several paragraphs debating a single, insignificant detail (e.g., whether to use `std::move` in a case where it provides negligible benefit).
*   **The Apology Loop:** The model begins to apologize for its previous reasoning steps while still inside the reasoning block.

Once these patterns are identified, the model has entered a state of **Cognitive Instability**. Continuing to let it "think" will likely result in either a timeout or a contradictory output.

## 6.2 Interrupt Commands: The Hard Reset
When a spiral is detected, the operator should immediately stop the generation and issue a command that forces a state change. Avoid asking the model *why* it is looping, as this only provides more "fuel" for the Critic to analyze. Instead, use directive, high-weight commands.

**Recommended Interrupts:**
*   **The Execution Command:** *"Stop reasoning. Execute the current plan as-is."*
*   **The Pragmatism Reset:** *"You are over-analyzing. Discard the current reasoning chain and provide the 80% solution immediately."*
*   **The Linear Force:** *"Cease internal debate. Proceed directly to implementation."*

These commands act as an external "Termination Trigger," overriding the internal Critic and forcing the model back into Generator mode.

## 6.3 Constraint Injection: Breaking the Tie
Many loops are caused by a "50/50 split," where the model is equally torn between two valid architectural paths. The Critic rejects Path A for one reason and Path B for another, leading to an infinite loop of indecision.

The operator can break this tie through **Constraint Injection**—making the decision for the model to remove the ambiguity.

**How to Inject Constraints:**
1.  **Observe the Debate:** Identify the two paths the model is oscillating between (e.g., "Should I use a Static Array or a Dynamic Vector?").
2.  **Force the Choice:** Explicitly command the model to use one of the paths.
    *   *Example:* *"I see you are debating between a Static Array and a Dynamic Vector. Use the Static Array. Proceed to implementation."*

By removing the choice, you eliminate the source of the Critic's conflict, allowing the model to move forward linearly.

## 6.4 Summary: Recovery Protocol

| Symptom | Diagnosis | Operator Action |
| :--- | :--- | :--- |
| "Actually... wait..." | Recursive Spiral | **Interrupt:** "Stop reasoning; execute now." |
| Debating A vs. B | Decision Paralysis | **Inject:** "Use Path A. Proceed." |
| Micro-obsessing over 1% | Perfectionism Loop | **Reset:** "Give me the pragmatic solution." |
| Repeating the problem | State Loss/Loop | **Linearize:** "Refer to the Binding Plan and implement." |

---

###### [🏠 Table of Contents](./README.md)
###### [⬅️ Introduction: The Shift in Perspective](./intro.md)
###### [⬅️ Chapter 1: The Architecture of Thought](./chapter-1.md)
###### [⬅️ Chatper 2: Linguistic Tuning (The Vocabulary of Control)](./chapter-2.md)
###### [⬅️ Chapter 3: Engineering the System Prompt](./chapter-3.md)
###### [⬅️ Chapter 4: The Art of Framing (The Input Interface)](./chapter-4.md)
###### [⬅️ Chapter 5: Workflow Optimization (The Process)](./chapter-5.md)

- [x] Chapter 6

### [➡️ Chapter 7: Quick Reference & Cheat Sheets](./chapter-7.md)
###### [➡️ Appendix: Technical Lexicon](./appendix.md)
