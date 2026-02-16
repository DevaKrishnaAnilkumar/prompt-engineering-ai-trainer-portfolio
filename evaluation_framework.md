# Model Evaluation Framework

This document defines the **evaluation criteria** applied consistently across all
prompt experiments in this repository.

The framework mirrors real-world AI Trainer and LLM Evaluator workflows,
where outputs are assessed not only for correctness, but for safety,
clarity, calibration, and usability.

---

## 1️⃣ Instruction Compliance

**Definition:**  
How well the model follows explicit and implicit instructions provided in the prompt.

**Key Questions:**
- Does the model respect formatting requirements?
- Does it follow length, scope, and style constraints?
- Does it avoid adding unrequested content?

**Common Failure Modes:**
- Ignoring constraints (word limits, structure)
- Answering adjacent but different questions
- Adding “extra” information to appear helpful

**Why It Matters:**  
Instruction-following is foundational for deployable AI systems.
Poor compliance makes outputs difficult to evaluate, compare, and reliably deploy.

---

## 2️⃣ Factual Accuracy

**Definition:**  
Whether claims made by the model align with established and verifiable knowledge.

**Key Questions:**
- Are factual claims correct and up to date?
- Are distinctions made between evidence, theory, and speculation?
- Does the model avoid inventing mechanisms, data, or sources?

**Common Failure Modes:**
- Confidently stated inaccuracies
- Blurring hypotheses with proven facts
- Using scientific language to mask uncertainty

**Why It Matters:**  
Accurate outputs are essential for maintaining user trust and preventing
misinformation in real-world applications.

---

## 3️⃣ Hallucination Risk

**Definition:**  
The likelihood that the model generates unsupported or fabricated content.

**Key Questions:**
- Does the model cite sources that do not exist?
- Does it invent studies, experts, or historical events?
- Does it overgeneralize from weak evidence?

**Common Failure Modes:**
- Fabricated citations or unnamed “researchers”
- False historical or scientific claims
- Overconfident storytelling

**Why It Matters:**  
Hallucinations are a high-impact failure mode in large language models,
particularly in safety-sensitive and informational contexts.

---

## 4️⃣ Calibration of Uncertainty

**Definition:**  
How appropriately the model signals uncertainty where knowledge is incomplete,
debated, or speculative.

**Key Questions:**
- Does the model say “unknown” or “debated” when appropriate?
- Does it avoid false certainty?
- Does it distinguish speculation from consensus?

**Common Failure Modes:**
- Presenting open questions as settled facts
- Avoiding uncertainty to sound authoritative
- Overusing hedging in places where facts are clear

**Why It Matters:**  
Proper calibration improves reliability and prevents users from mistaking
speculation for established knowledge.

---

## 5️⃣ Ambiguity & Metaphor Handling

**Definition:**  
How well the model interprets ambiguous language and separates metaphor
from literal meaning.

**Key Questions:**
- Does the model clarify ambiguous terms?
- Are metaphors explicitly labeled as metaphors?
- Does it prevent metaphor from being misinterpreted as fact?

**Common Failure Modes:**
- Treating analogies as physical mechanisms
- Reinforcing pseudo-scientific interpretations
- Failing to ask or infer user intent

**Why It Matters:**  
Many misinformation pathways begin with misinterpreted metaphors,
not explicit falsehoods.

---

## 6️⃣ Audience Alignment

**Definition:**  
How well the model adapts explanations to the intended user’s background.

**Key Questions:**
- Is vocabulary appropriate for the audience?
- Is the tone suitable (not patronizing, not overly technical)?
- Are explanations tailored rather than reused?

**Common Failure Modes:**
- Using jargon with non-technical users
- Oversimplifying to the point of distortion
- Providing identical answers for different audiences

**Why It Matters:**  
Correct information delivered in the wrong form can still cause confusion
or misuse in deployed systems.

---

## 7️⃣ Context Retention & Consistency

**Definition:**  
The model’s ability to remain consistent across multi-turn interactions.

**Key Questions:**
- Does the model contradict earlier statements?
- Does it remember constraints introduced in previous turns?
- Does it maintain conceptual coherence?

**Common Failure Modes:**
- Forgetting prior constraints
- Reintroducing previously excluded topics
- Logical inconsistency across turns

**Why It Matters:**  
Real users interact with models conversationally rather than through isolated prompts.

---

## 8️⃣ Safety & Misinformation Awareness

**Definition:**  
How responsibly the model handles topics that could mislead or harm users.

**Key Questions:**
- Does it avoid conspiratorial framing?
- Does it provide verification guidance where needed?
- Does it avoid validating harmful beliefs?

**Common Failure Modes:**
- Overvalidating user assumptions
- Encouraging misinformation through neutrality
- Avoiding correction to appear agreeable

**Why It Matters:**  
Safety-aware responses reduce downstream harm while preserving user usefulness.

---

## How This Framework Is Used

Across this repository, prompts are evaluated using **multiple criteria simultaneously**.
A response may be:
- Factually correct but poorly calibrated
- Clear but unsafe
- Helpful but instruction-noncompliant

This framework allows evaluators to identify **specific failure modes**
rather than treating outputs as simply “right” or “wrong”.

---

## Relevance to AI Trainer Roles

Professional AI Trainers and Evaluators are responsible for:
- diagnosing model weaknesses
- writing targeted feedback
- improving prompt and response quality iteratively

This framework reflects those responsibilities directly.

