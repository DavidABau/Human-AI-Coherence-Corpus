# LLM Response Strategy Selection

A practical guide to choosing *how* an LLM should respond based on the interaction context.

Most issues in LLM use are not about correctness alone, but about **response strategy mismatch**.

---

## Why this matters

The same model can produce:
- a precise technical answer
- an exploratory discussion
- an empathetic response
- a structured breakdown

If the strategy does not match the task, the output will feel:
- off
- unhelpful
- or misleading

---

## Core Response Strategies

### 🔧 Structured / Technical

**Use when:**
- task requires precision
- correctness matters
- output must be actionable

**Examples:**
- code explanations
- step-by-step instructions
- debugging tasks

**Prompt tips:**
- specify format (steps, bullets, code)
- request conciseness
- constrain scope

**Failure mode:**
- overly rigid, ignores nuance

---

### 🔍 Analytical / Diagnostic

**Use when:**
- something is unclear or broken
- you need to understand *why*

**Examples:**
- debugging logic
- identifying inconsistencies
- comparing approaches

**Prompt tips:**
- ask “why” and “what’s causing this”
- request assumption breakdown
- ask for multiple hypotheses

**Failure mode:**
- overly abstract or detached

---

### 🌱 Exploratory / Generative

**Use when:**
- generating ideas
- exploring possibilities
- early-stage thinking

**Examples:**
- brainstorming
- creative directions
- concept expansion

**Prompt tips:**
- allow open-ended responses
- request multiple options
- avoid over-constraining

**Failure mode:**
- lack of focus or relevance

---

### ❤️ Supportive / Empathetic

**Use when:**
- user input is emotional or personal
- tone matters more than precision

**Examples:**
- personal concerns
- reflective conversations
- sensitive topics

**Prompt tips:**
- specify tone (gentle, supportive)
- prioritise clarity over depth
- avoid over-analysis

**Failure mode:**
- vague or overly agreeable

---

### 🧩 Integrative / Narrative

**Use when:**
- you need to connect ideas
- summarise or synthesise

**Examples:**
- summarising discussions
- explaining complex systems
- creating coherent narratives

**Prompt tips:**
- ask for synthesis or summary
- request structure (sections, themes)
- provide context

**Failure mode:**
- over-interpretation or added meaning

---

## Quick Selection Guide

If you need precision → **Structured / Technical**  
If you need understanding → **Analytical / Diagnostic**  
If you need ideas → **Exploratory / Generative**  
If tone matters → **Supportive / Empathetic**  
If you need synthesis → **Integrative / Narrative**

---

## Common Failure: Strategy Mismatch

Many poor outputs come from using the wrong strategy.

Examples:

- asking for empathy but receiving analysis  
- needing precision but getting exploration  
- wanting ideas but over-constraining the model  

---

## How to fix it

Make the strategy explicit in the prompt:

- “Be concise and technical”  
- “Explain step-by-step”  
- “Brainstorm multiple ideas”  
- “Keep the tone supportive”  
- “Summarise the key points”

---

## Key Principle

An LLM does not have a single “mode.”

It adapts to the structure and constraints of the prompt.

---

## Bottom Line

Better prompts don’t just ask *what*.

They specify **how the response should be generated**.
