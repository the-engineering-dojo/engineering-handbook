# 🤖 Use AI without outsourcing your understanding

[← Notes](README.md)

We use AI tools. But speed is not the same as skill.

### 🔄 A practical learning protocol

**1. Predict:** Before asking an assistant, write what you think will happen.

**2. Ask for alternatives:** Request counterexamples, failure conditions, or trade-offs—not just a finished solution.

**3. Verify:** Check primary documentation, reproduce claims, and inspect behavior.

**4. Rebuild:** Explain the result to a teammate without relying on generated text.

**5. Review:** Ask another person to challenge an assumption.

### ✅ Productive AI prompts

- “Here is my concurrency strategy. Find a failing interleaving.”
- “Ask me diagnostic questions instead of writing the code.”
- “What experiment could falsify my architecture claim?”
- “Compare failure modes, but make the uncertainty explicit.”

### 🚫 Patterns to avoid

- Copying architecture diagrams you cannot explain.
- Adding patterns just because a model suggested them.
- Treating AI-generated tests as proof without checking test coverage of the invariant.
- Letting an assistant silently choose the requirements.

**Team rule:** AI is a tool; the contributor owns the understanding, verification, and review.