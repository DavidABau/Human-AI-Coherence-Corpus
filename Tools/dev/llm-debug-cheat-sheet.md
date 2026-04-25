# LLM Debug Cheat Sheet

A quick reference for diagnosing and fixing common LLM interaction issues.

Use this during prompting, debugging, or evaluation.

---

## 1. What’s wrong?

| Symptom | Likely Issue |
|--------|-------------|
| Messy / vague output | Input Coherence Failure |
| Repeating / looping | Resolution Failure |
| Feels off | Context Misalignment |
| Overconfident answer | Premature Convergence |
| Confident but wrong | Stabilized Incoherence |
| Wrong tone / style | Strategy Mismatch |

---

## 2. What to fix

### Input Coherence
- simplify prompt
- split tasks
- define output format

---

### Context Misalignment
- define key terms
- restate intent
- provide examples

---

### Resolution Failure
- add constraints
- request step-by-step reasoning
- anchor the task

---

### Premature Convergence
- ask for alternatives
- request self-critique
- test assumptions

---

### Stabilized Incoherence
- ask for sources
- cross-check externally
- tighten constraints

---

### Strategy Mismatch
- specify tone (technical, concise, supportive)
- separate tasks (analysis vs emotion)
- define response format

---

## 3. Strategy selection

| Need | Strategy |
|------|---------|
| Precision | Structured / Technical |
| Understanding | Analytical / Diagnostic |
| Ideas | Exploratory / Generative |
| Tone sensitivity | Supportive / Empathetic |
| Synthesis | Integrative / Narrative |

---

## 4. Quick loop

1. Identify the symptom  
2. Map to failure type  
3. Apply the fix  
4. Adjust response strategy  
5. Re-test  

---

## Key Principle

Most LLM failures are not model failures.

They are:
- input issues
- interaction issues
- or untested convergence

---

## Bottom Line

> Debug the interaction, not just the model.
