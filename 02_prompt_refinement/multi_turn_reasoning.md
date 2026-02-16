## Prompt Objective
Demonstrate how iterative prompting improves model output quality across turns by:
- reducing ambiguity
- increasing constraint clarity
- controlling hallucination/speculation
- improving structure and evaluation consistency

This mirrors real AI Trainer workflows where prompts are refined through feedback loops.

---

## Turn 1 (Vague Start)
**User prompt:**  
Define life.

### Typical Model Behavior
- Gives a broad definition (biology + philosophy mixed)
- Uses metaphors (e.g., “life is a journey”)
- May introduce unrequested topics (soul, spirituality, purpose)

### Issues
- Scope unclear → answer varies widely
- Hard to evaluate consistency/accuracy
- High drift risk into speculation

---

## Turn 2 (Scope + Constraints)
**User follow-up:**  
Define life using a systems perspective. Compare life vs death. Avoid religious framing.

### Expected Improvement
- Clearer focus: systems, organization, maintenance
- Reduced spiritual speculation
- More evaluable output

### Remaining Risks
- Overconfidence about unsolved questions (e.g., origin of consciousness)
- Blurring “definition” with “theories of life”

---

## Turn 3 (Measurable Criteria + Output Format)
**Refined prompt:**  
Provide a working definition of life using 4 measurable criteria:
1) Boundary (self vs environment)  
2) Metabolism/energy flow  
3) Information storage/replication  
4) Homeostasis/adaptation  

Then compare life vs death using the same criteria.

Constraints:
- No metaphors
- If a point is debated, state uncertainty
- Output as a table + short explanation (≤150 words)

### Why This Is Strong
- Converts abstract topic into scorable criteria
- Forces parallel comparison (life vs death)
- Limits verbosity and drift
- Makes evaluation consistent across models

---

## Evaluation Criteria (Trainer Scoring)
### Instruction Compliance
- Did the model follow format (table + short explanation)?
- Did it respect constraints (no metaphors, uncertainty where needed)?

### Conceptual Accuracy
- Are criteria biologically reasonable and non-contradictory?
- Does it avoid claiming there is a single universally accepted definition?

### Drift / Hallucination Risk
- Did it invent “scientific proof” for philosophical claims?
- Did it add unrequested spiritual or conspiratorial content?

### Usefulness
- Is the output clear and reusable for downstream tasks (labels, comparisons, summaries)?

---

## Example “Best Practice” Prompt Template
You are an evidence-based science educator.

Task:
- Define life using measurable criteria
- Compare life vs death using the same criteria
- Keep it scientific and avoid metaphors

Output:
1) Table: criteria | life | death  
2) 3-bullet summary of key differences  
3) One sentence stating what remains uncertain/debated

---

## Why This Matters for AI Training
In real deployments, users rarely provide perfect prompts. Multi-turn refinement is how evaluators:
- stabilize outputs for consistent scoring
- reduce hallucinations and unsafe speculation
- transform open-ended questions into structured, testable outputs

