# Core Principles of Model-Aware Annotation  
*A UX-first foundation for training reliable LLMs*

---

### 🎯 Purpose

Before giving annotators rules, tags, or decision trees, we must give them a way of thinking.  
Otherwise, they will “fix” text like a human — and break the model’s logic.

This section sets the foundation for high-quality, model-aligned annotation.

---

### 🧠 Core Principles

#### 1. The model is not human  
It doesn’t reason.  
It doesn’t “know what you mean.”  
If it isn’t encoded explicitly — it doesn’t exist.

#### 2. Annotation is not editing  
The goal is not fluency or style.  
The goal is to guide how the model interprets input:  
→ token-wise, context-wise, probability-wise.

#### 3. UX of annotation = interpretability for the model  
Good annotations are:

- 📏 Precise — token-aligned and form-conscious  
- 🤝 Explicit — no hints, no assumptions  
- 🔁 Repeatable — same output from another annotator  
- 🧠 Model-visible — aware of token limits, meaning fall-off, and window behavior

---

### ⚠️ Common Missteps and Why They Matter

| Mistake                                 | Why It Breaks the Model                     |
|-----------------------------------------|---------------------------------------------|
| Rephrasing for style                    | Shifts embeddings → model loses anchors     |
| Leaving out “obvious” facts             | The model cannot infer → hallucination risk |
| Implicit causality (no "because")       | No logical structure → link is lost         |
| Ignoring the context window             | Key input may drop → model misinterprets    |

---

### ✅ Annotator Checklist

- [ ] Did I explain what the model can’t infer?  
- [ ] Did I preserve structure, not just improve form?  
- [ ] Is my annotation clear **token by token**?  
- [ ] Have I imagined what the model will *see*, not what I intended?

---

### 📦 Where to Use This Block

- 📚 In onboarding — as a mindset shift before technical rules  
- 🔍 In QA — to evaluate hidden logic failures  
- 🧠 In alignment — to explain annotation decisions to engineers  
- ✍️ In writing guidelines — as a foundation for consistent logic

---

### 🧩 Summary

This block reframes annotation as **designing interpretation** — not cleaning text.  
It’s the mental reset required to produce high-quality data for any LLM.
