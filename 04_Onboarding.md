# UX-Oriented onboarding for annotation teams  
*A repeatable, logic-driven training module for LLM-facing workflows*

---

### 🎯 Why this block matters

Most annotation errors don’t come from carelessness —  
they come from applying human reasoning to model-facing tasks.

This block provides a structured path to onboard new annotators using:

- UX-oriented mindset  
- Examples rooted in model behavior  
- Repeatable cases instead of abstract rules

---

### 🗺️ Core skill map for annotators

To align with model needs, annotators must:

- Understand what the model “sees” — tokens, embeddings, probabilities  
- Avoid human logic (“this sounds positive”)  
- Apply tagging systems consistently  
- Know when to stop and flag ambiguity instead of guessing

---

### 📚 Training principles

- Teach through **behavioral outcomes**, not rule memorization  
- Use real-world examples where annotation affects generation  
- Build **“mental muscle”** for asking:  
  → *“Will the model see this?”*  
  → *“What does this annotation teach the model?”*

---

### 💡 Microcase: Why “Obvious” Doesn’t Mean “Model-Visible”

> Sentence: **“Oh yes. Very professional.”**

**New annotator’s instinct:**  
→ Tags it as `sentiment.positive` — because the words are flattering

**Why this breaks the model:**  
→ The model sees only token-level signals. Without irony markers, it learns that this phrase = praise

**Correct UX-aware annotation:**  
→ Tag as `irony.explicit`

**Lesson:**  
When surface tokens contradict the true intent, don’t trust your human gut —  
ask: *“How would the model interpret this, without context?”*

---

### 🚫 Common beginner errors (and how to prevent them)

| Mistake                            | Prevention strategy                                |
|------------------------------------|----------------------------------------------------|
| Annotating for humans, not models | Start with Block 1: “how the model thinks”         |
| Tagging “by feel”                 | Use decision trees (see Block 3)                   |
| Rewriting instead of guiding      | Explain: annotation is **design**, not correction  |
| Avoiding edge cases               | Teach to flag, not ignore                         |

---

### 🧩 QA and coaching loop

- Use microcases as spot checks during early QA  
- Collect unclear examples for team review  
- Make ambiguity a discussion point — not a punishment

---

### 📦 Where to use this block

- When onboarding new annotators  
- When scaling to new languages or cultural domains  
- As internal documentation for AI/UX collaboration  
- As a foundation for building multilingual annotation guides

---
