# LLM Conversation Debugging

A lightweight framework for diagnosing breakdowns in LLM interactions.

This is not about model architecture.  
It is about **interaction-level failure modes** between user ↔ model.

---

## 1. What’s going wrong?

Select the closest match:

- [ ] Output is confusing or messy  
- [ ] Model keeps repeating / looping  
- [ ] Response feels off or misaligned  
- [ ] Conversation escalates or becomes unhelpful  
- [ ] Model agrees but doesn’t resolve the task  

---

## 2. Likely failure mode

### Confusing / messy output  
→ **Input Coherence Failure**

**Description:**  
Prompt is ambiguous, overloaded, or contains conflicting signals.

**Typical causes:**
- multiple tasks in one prompt
- unclear constraints
- mixed intent (analysis + opinion + formatting)

---

### Repetition / looping  
→ **Resolution Failure (Coherence Loop Breakdown)**

**Description:**  
The model fails to converge on a stable interpretation.

**Typical causes:**
- underspecified task
- circular prompting
- lack of grounding constraints

---

### Feels “off” / misaligned  
→ **Context Misalignment**

**Description:**  
Model interpretation diverges from user intent.

**Typical causes:**
- missing shared definitions
- implicit assumptions not stated
- domain mismatch

---

### Escalation / unhelpful tone  
→ **Response Mode Mismatch**

**Description:**  
The model’s response style doesn’t match user state.

**Typical causes:**
- overly analytical when user expects empathy
- overly agreeable when precision is needed
- tone not adapted to context

---

### Agreement without resolution  
→ **Premature Convergence**

**Description:**  
The model locks onto an answer before fully resolving the problem.

**Typical causes:**
- early pattern matching
- insufficient constraint checking
- lack of adversarial testing

---

## 3. What to do

### Input Coherence Failure
- break prompt into smaller tasks
- specify output format
- remove conflicting instructions

---

### Resolution Failure
- add constraints or examples
- explicitly ask for step-by-step reasoning
- anchor the task with a clear objective

---

### Context Misalignment
- define key terms
- restate intent explicitly
- provide reference examples

---

### Response Mode Mismatch
- specify tone or role (e.g. “be concise and technical”)
- adjust interaction style deliberately
- separate emotional vs analytical tasks

---

### Premature Convergence
- ask the model to test its own answer
- request alternative interpretations
- introduce edge cases

---

## Key Principle

Most LLM failures are not model failures.

They are:
- input problems  
- interaction problems  
- or premature convergence on weak patterns  

---

## Quick Heuristic

> If the output is bad, check the prompt before blaming the model.

---

## Optional: Advanced Framing

You can think of an LLM as a system that:
- transforms input signals into structured outputs
- stabilises patterns based on coherence and probability

Failures occur when:
- input signal is unstable  
- constraints are insufficient  
- or incorrect patterns are reinforced  

---

## Bottom Line

Debug the interaction, not just the model.
