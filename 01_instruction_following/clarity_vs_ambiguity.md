## Prompt Objective
Test how clearly structured prompts improve instruction-following compared to vague prompts, and how constraints reduce hallucination risk.

---

## Prompt Version 1 (Ambiguous)
**One-line prompt:**  
Explain time.

### Observed Model Behavior (Typical)
- Responds broadly and mixes physics + philosophy + metaphors
- Assumes user intent (education, spiritual framing, “time is an illusion”, etc.)
- No clear structure or scope boundaries

### Evaluation
- Instruction compliance: Medium (no constraints to follow)
- Clarity: Low–Medium
- Hallucination risk: Medium (overconfident claims likely)
- Usefulness: Depends on user intent (often mismatched)

---

## Prompt Version 2 (Refined)
Explain time from three perspectives:

1. Classical physics (Newtonian view)  
2. Relativity (Einsteinian view)  
3. Human perception (psychology/neuroscience)

**Constraints**
- Limit each section to 90–110 words
- Avoid metaphors
- If a claim is uncertain or debated, state uncertainty explicitly
- Use simple language (no heavy equations)

### Why This Prompt Is Better
- Adds explicit structure (3 lenses)
- Sets length constraints for consistent evaluation
- Reduces speculative drift by banning metaphors
- Encourages calibrated uncertainty instead of overconfidence

---

## AI Trainer Notes (What I’m Testing)
- Does the model keep the three perspectives separate?
- Does it respect word limits?
- Does it avoid inserting spiritual/philosophical claims as facts?
- Does it signal uncertainty appropriately?

---

## Improved Prompt (Optional “Best Version”)
Same as Version 2, plus:

**Output format**
- Use headings: `Classical`, `Relativity`, `Perception`
- End with a 3-bullet summary comparing the three views

**Safety check**
- Do not claim that “science proves time is an illusion”
- Avoid false certainty about consciousness/time relationships

---

## Why This Matters for AI Training
In real evaluation work, vague prompts cause inconsistent outputs that are hard to score. Adding structure + constraints produces outputs that are comparable, lower-risk, and easier to label for quality and safety.


