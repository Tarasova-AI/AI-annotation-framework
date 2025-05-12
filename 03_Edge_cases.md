# Handling ambiguity and conflict in annotation  
*Decision logic for cases that don’t fit the rules*

---

### 🎯 Why this block matters

No guideline covers 100% of cases.  
But **imprecise annotation** in an edge case can lead to **skewed training and costly model errors**.

This block gives annotators a structured way to act — not guess — when:

- tags overlap,  
- context is unclear,  
- or cultural differences create ambiguity.

---

### ⚠️ Common types of edge cases

#### 🌀 1. Overlapping categories  
Example: a sentence is both sarcastic and negatively toned.  
→ Which tag takes priority?

#### 🌍 2. Cross-cultural or language-specific differences  
Example: a Russian idiom like “моя хата с краю” may read as neutral, ironic, or evasive depending on the reader.  
→ Should this be tagged as `idiom`, `irony`, or neither?

#### 🧩 3. Lack of context  
Example: “That was interesting.”  
→ Is it positive? Sarcastic? Neutral? Do we mark it or skip it?

#### 🔀 4. Instruction vs. annotator intuition  
Example: a phrase is flagged as `offensive`, but might be a joke within a specific group.  
→ Follow the letter of the rule — or account for context?

---

### 🧠 Resolution strategies

#### 1. **Use decision trees, not gut feelings**  
Structured logic improves inter-annotator consistency and model alignment.

#### 2. **Flags are not failures**  
Using `ambiguous`, `cross-cultural`, or `requires-context` isn’t weak —  
it’s how we prevent silent model drift.

#### 3. **Separate what’s seen from what’s inferred**  
Even if a human can “sense” the tone, ask:  
→ *Will the model see it in the input — or hallucinate?*

---

### 🌳 How to build a decision tree

1. Identify the pain point:  
   What’s unclear — semantics, tone, cultural anchor?

2. Build logical checkpoints:  
   “Are there clear markers?” → “Can it be understood in isolation?” → “Is it token-visible?”

3. Each endpoint leads to:
- A specific tag  
- A fallback flag (`ambiguous`, `cross-cultural`, `requires-context`)  
- Or exclusion from annotation

---

### 🔎 Example: irony decision tree

```plaintext
Are there explicit lexical irony markers?
  └─ Yes → irony.explicit
  └─ No →
      Compare meaning vs. context:
        └─ Contradiction is present but unprovable → ambiguous
        └─ Interpretation depends on cultural frame → cross-cultural
        └─ Meaning depends on external knowledge → requires-context
