# Annotating Across Languages: Token-aware, Culture-aware, Model-aware  
*A practical guide for multilingual annotation workflows*

---

### 🌟 Why this block matters

Multilingual data is not “just more text.”
It changes how models tokenize, interpret, and hallucinate.

This block teaches how to annotate:

- With awareness of token length differences
- With cultural interpretation in mind
- With language-specific risks (grammar, idioms, meaning collapse)

---

### 🧠 Language affects everything

| Language | Token density | Risk profile                                     |
|----------|----------------|--------------------------------------------------|
| English  | Low            | Efficient for long chunks                        |
| French   | Medium         | Watch for idioms and gendered ambiguity          |
| Russian  | High           | Token cost is high; structure is more fragile    |

🚧 Russian can use 2x more tokens per sentence → shorter chunks, faster context drop

---

### ⚖️ Cultural variation: same sentence, different world

> "I told my boss the truth."

- In some contexts: honesty = integrity
- In others: truth-telling = insubordination

Use flags:
- `cross-cultural` if the interpretation depends on cultural frame
- `requires-context` if surrounding norms are missing

---

### 🔹 Grammar traps in multilingual annotation

- **Negation scope** varies by language → tag it explicitly (`negation.scope`)
- **Tense mismatch** is easy to miss when translating
- **Idioms** may appear literal → use `idiom.lost` or `idiom.transferred`
- **Pronoun ambiguity** increases in languages with gendered or dropped subjects

---

### ✅ Checklist for multilingual annotation

- [ ] Did I account for token inflation across languages?
- [ ] Did I chunk based on token count, not word count?
- [ ] Did I preserve logic, not just translate tone?
- [ ] Did I flag culturally sensitive or ambiguous areas?

---

### 📦 Where this block helps

- In annotation for translation, QA, or multilingual generation
- When training annotators unfamiliar with linguistic drift
- In designing language-specific review pipelines

---
