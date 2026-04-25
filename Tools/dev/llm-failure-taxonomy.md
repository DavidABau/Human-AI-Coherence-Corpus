# LLM Failure Taxonomy

A practical classification of common failure modes in LLM interactions.

This taxonomy focuses on **interaction-level failures**, not model architecture.

It helps answer:
> What kind of failure is this, and how should it be addressed?

---

## 1. Input Coherence Failure

**Description:**  
The prompt is ambiguous, overloaded, or internally inconsistent.

**Symptoms:**
- vague or unfocused output
- partial or conflicting responses
- model “guessing” intent

**Common causes:**
- multiple tasks in one prompt
- unclear constraints
- mixed intent (analysis + opinion + formatting)

**Fix:**
- simplify the prompt
- separate tasks
- specify output structure

---

## 2. Context Misalignment

**Description:**  
The model interprets the prompt differently than intended.

**Symptoms:**
- technically correct but irrelevant answers
- wrong assumptions
- drifting away from the task

**Common causes:**
- missing definitions
- unstated assumptions
- insufficient context

**Fix:**
- define key terms
- restate intent explicitly
- provide examples or references

---

## 3. Resolution Failure (Non-Convergence)

**Description:**  
The model fails to stabilise on a coherent output.

**Symptoms:**
- repetition or looping
- circular reasoning
- incomplete answers

**Common causes:**
- underspecified task
- lack of constraints
- conflicting instructions

**Fix:**
- add constraints
- request step-by-step reasoning
- anchor with a clear objective

---

## 4. Premature Convergence

**Description:**  
The model settles on an answer too early without sufficient validation.

**Symptoms:**
- shallow or incomplete answers
- overconfident conclusions
- lack of alternative perspectives

**Common causes:**
- pattern matching without verification
- insufficient constraint checking
- no adversarial prompting

**Fix:**
- ask for alternative interpretations
- request self-critique
- introduce edge cases

---

## 5. Stabilized Incoherence (Confident Hallucination)

**Description:**  
The model produces a stable, confident output that is incorrect or misaligned with reality.

**Symptoms:**
- confident but wrong answers
- fabricated details
- internally consistent but externally false explanations

**Common causes:**
- weak grounding
- lack of external reference
- reinforcement of incorrect patterns

**Fix:**
- request sources or verification
- cross-check with external data
- reframe the question with stricter constraints

---

## 6. Response Strategy Mismatch

**Description:**  
The model uses the wrong response style for the task.

**Symptoms:**
- overly technical when simplicity is needed
- overly vague when precision is required
- emotionally inappropriate tone

**Common causes:**
- strategy not specified in prompt
- mixed user intent
- unclear expectations

**Fix:**
- explicitly define response style
- separate analytical vs emotional tasks
- guide tone and format

---

## Key Principle

Not all failures are equal.

Different failure modes require different fixes.

---

## Quick Debug Heuristic

1. Is the input clear? → **Input Coherence**  
2. Is the interpretation correct? → **Context Misalignment**  
3. Is the output stable? → **Resolution Failure**  
4. Is the answer tested? → **Premature Convergence**  
5. Is it confidently wrong? → **Stabilized Incoherence**  
6. Does the style fit? → **Strategy Mismatch**

---

## Bottom Line

Most LLM issues can be traced to:
- input problems  
- interaction design  
- or untested convergence  

Debug the interaction before blaming the model.
