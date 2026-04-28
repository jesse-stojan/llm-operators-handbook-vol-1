#### [🏠 Table of Contents](./README.md)

###### [⬅️ Chapter 7: Quick Reference & Cheat Sheets](./chapter-7.md)

---

# Appendix: Technical Lexicon

This appendix defines the specific terminology and idioms used throughout this handbook.

### From Chapter 1: The Architecture of Thought
*   **Chain-of-Thought (CoT):** A reasoning process where the model generates intermediate logical steps before arriving at a final conclusion.
*   **Token:** The atomic unit of text (a character, word, or sub-word) that an LLM processes as a numerical vector.
*   **Search Space:** The total set of all possible solutions, paths, or configurations the model evaluates when trying to find an answer.
*   **High-Gain Signal:** In this context, a prompt word that disproportionately amplifies a specific internal behavior (e.g., "Optimal" amplifying the Critic).

### From Chapter 2: Linguistic Tuning
*   **Internal Weights:** The numerical parameters of the neural network that determine the strength and direction of a signal between neurons.
*   **Recursive:** A process that calls or refers back to itself; in LLMs, this refers to the loop of self-correction that fails to terminate.

### From Chapter 3: Engineering the System Prompt
*   **RAII (Resource Acquisition Is Initialization):** A C++ idiom ensuring that resources are tied to object lifetime, preventing memory leaks.
*   **Termination Trigger:** A specific condition or instruction that signals the model to stop a process (like reasoning) and move to the next state.
*   **Signal-to-Noise Ratio:** The ratio of useful information (signal) to irrelevant filler or conversational fluff (noise).

### From Chapter 4: The Art of Framing
*   **Latency:** The time elapsed between a request and the start of the response (the "delay").
*   **Throughput:** The volume of data or number of requests a system can process within a specific time frame.
*   **Objective Constraint:** A binary requirement (Yes/No) that removes ambiguity, as opposed to a subjective goal (Better/Faster).

### From Chapter 5: Workflow Optimization
*   **Compilation Unit:** A source file and all its included headers that are processed by a compiler into a single object file.
*   **Few-Shot Prompting:** The technique of providing a few high-quality examples of a desired input/output pair to guide the model's behavior.
*   **State Overflow:** A metaphorical term for when the model's internal context becomes too cluttered with conflicting goals, leading to a reasoning collapse.

### From Chapter 6: Real-Time Supervision
*   **Reasoning Trace:** The visible "thought" block where the model documents its internal logic before generating a final response.
*   **Constraint Injection:** The act of manually introducing a hard limitation mid-conversation to break a tie or a loop.


###### [🏠 Table of Contents](./README.md)
###### [⬅️ Introduction: The Shift in Perspective](./intro.md)
###### [⬅️ Chatper 2: Linguistic Tuning (The Vocabulary of Control)](./chapter-2.md)
###### [⬅️ Chapter 3: Engineering the System Prompt](./chapter-3.md)
###### [⬅️ Chapter 4: The Art of Framing (The Input Interface)](./chapter-4.md)
###### [⬅️ Chapter 5: Workflow Optimization (The Process)](./chapter-5.md)
###### [⬅️ Chapter 6: Real-Time Supervision (Course Correction)](./chapter-6.md)
###### [⬅️ Chapter 7: Quick Reference & Cheat Sheets](./chapter-7.md)

- [x] Appendix
