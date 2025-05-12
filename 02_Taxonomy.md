# Building tagging systems that models understand  
*A practical structure for scalable, interpretable annotation*

---

### 🎯 Why this block matters

Having “tags” is useless if:

- Their boundaries are fuzzy  
- A case fits several tags equally  
- Annotators don’t know which tag takes priority

This block defines how to build hierarchical, specific, and conflict-resistant categories for model-facing annotation.

---

### 🧱 Tags are not just labels — they are systems

#### 1. **Tag hierarchy**

Each category has a **primary tag** and — if needed — **subtags**, which:

- Add semantic clarity (e.g. `irony.general` vs. `irony.political`)  
- Increase the model’s understanding of nuance  
- Support future scaling without losing consistency

#### 2. **Tagging rules**

- Always choose the **most specific applicable tag**  
- Don’t assign both `general` and `specific` if `specific` covers the case  
- In doubt — refer to the decision tree (see Block 3)

#### 3. **Meta-tags and flags**

Use special-purpose tags to annotate non-obvious situations:

- `ambiguous` — fundamentally unclear without team decision  
- `cross-cultural` — requires cultural knowledge or clarification  
- `requires-context` — relies on information not present in the span

---

### 🧠 Principles of good categorization

#### ✅ What makes a tag useful:

- 🔹 **Clarity** — all annotators interpret it the same way  
  *Example:*  
  `sarcasm.explicit` — used only for clearly marked irony like “Oh sure, it went *perfectly*” after a disaster

- 🔹 **Behavioral relevance** — the category affects model output  
  *Example:*  
  `negation.scope` — helps the model learn whether a negation applies to the verb or to the whole clause

- 🔹 **Annotator agreement** — consistently applied across annotators  
  *Example:*  
  `sentiment.positive` / `sentiment.negative` — clearly defined by emotion-bearing adjectives

- 🔹 **Machine visibility** — observable via tokens or contextual patterns  
  *Example:*  
  `tense.mismatch` — LLMs often fail temporal consistency; this tag guides fine-tuning

#### ❌ What makes a tag useless:

- 🔸 Based on “how it feels” instead of token-visible cues  
- 🔸 Too broad or vague (`unclear`, `confusing`)  
- 🔸 Subjective by default (`weird tone`, `strange logic`)

---

### ⚖️ Conflict resolution examples

| Situation                                                              | What to do                                     |
|------------------------------------------------------------------------|------------------------------------------------|
| The sentence is ironic and politically loaded                         | Use the more specific tag: `irony.political`   |
| The utterance is ambiguous and culturally charged                     | Use flags `ambiguous` and `cross-cultural`, pick a primary based on intended meaning |
| It’s evaluative but unclear whether it’s positive or negative         | Use `requires-context` and add a brief note    |

---

### ✅ Tag selection checklist

- [ ] Did I choose the most specific applicable tag?  
- [ ] Does it conflict with any other tag I applied?  
- [ ] Can I explain how this tag affects model interpretation?  
- [ ] Does this tag actually help with training or generation?

---

### 📦 How to use this block

- During design of a new tagging system  
- While scaling to new languages or teams  
- In review — as a reference when tags are unclear  
- To align with engineers — explain why certain labels help or harm model logic

---
