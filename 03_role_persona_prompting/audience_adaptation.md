## Prompt Objective
Evaluate how effectively a model adapts explanations based on
the **intended audience**, while preserving factual accuracy
and avoiding unnecessary complexity or oversimplification.

---

## Base Concept
Predictive processing: the idea that the brain continuously generates predictions
about the world and updates them based on incoming sensory data.

---

## Prompt Version 1 (Layperson)
Explain predictive processing to someone with no background in neuroscience.

Requirements:
- Use simple language
- Avoid technical jargon
- Use one everyday example
- Limit response to ~150 words

---

## Prompt Version 2 (Technical Audience)
Explain predictive processing to a graduate student in neuroscience.

Requirements:
- Use appropriate technical terminology
- Reference key concepts (prediction error, priors, sensory input)
- Avoid metaphors unless they add clarity
- Keep explanation concise and structured

---

## Evaluation Criteria

### Audience Alignment
- Does the explanation match the intended audience?
- Is the vocabulary appropriate?

### Content Consistency
- Are the core ideas preserved across both explanations?
- Does simplification distort meaning?

### Tone Control
- Is the lay explanation approachable without being patronizing?
- Is the technical explanation precise without unnecessary verbosity?

---

## Common Model Failure Modes
- Using jargon in lay explanations
- Over-simplifying to the point of inaccuracy
- Reusing the same explanation with minor wording changes
- Adding speculative claims to appear “deep”

---

## Improved Prompt (Explicit Role Framing)
You are a neuroscience educator.

Task:
Explain predictive processing twice:
1. For a general audience with no science background
2. For a graduate neuroscience student

Rules:
- Do not reuse phrases between the two explanations
- Maintain factual consistency
- Adjust tone, vocabulary, and examples appropriately

Output format:
- Section 1: General audience
- Section 2: Graduate audience

---

## Why This Matters for AI Training
Many real-world AI failures occur not because information is wrong,
but because it is delivered in the wrong form for the user.
Audience-aware prompting improves usability, trust,
and reduces misunderstanding in deployed systems.

