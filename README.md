# Prompt Engineering & AI Trainer Portfolio
**Devakrishna Anilkumar**

> Focus: Evaluating and improving AI behavior through structured prompting, constraint design, and failure-mode analysis.

This repository demonstrates **real-world prompt engineering and LLM evaluation workflows**, with emphasis on diagnosing model failures, enforcing constraints, and improving reliability, safety, and usability in conversational AI systems.

The work reflects scenarios commonly encountered in production environments, including:
- ambiguous user intent
- evolving multi-turn conversations
- role and audience variation
- misinformation-prone queries
- long-context reasoning drift

This portfolio is designed to demonstrate skills relevant to:
- **AI Trainer**
- **LLM Evaluator**
- **Prompt Engineer (Junior)**
- **AI Quality / Alignment Analyst**

---

## Core Skills Demonstrated
- Prompt design and iterative refinement  
- Instruction-following evaluation  
- Hallucination detection and mitigation  
- Ambiguity & metaphor handling  
- Long-context reasoning analysis  
- Audience-aware response evaluation  
- Evidence calibration & verification checklists  
- Safety-aware constraint design  

A centralized evaluation framework is included to ensure **consistent scoring across experiments**, mirroring professional LLM annotation and evaluation pipelines.

---

## How to Read This Repository
Each experiment mirrors real AI evaluation tasks and includes:
- prompt objective  
- original or intentionally ambiguous prompt  
- common model failure modes  
- evaluation criteria  
- refined or constrained prompt  
- explanation of why the case matters for AI training  

The emphasis is on **model behavior analysis**, not on showcasing model outputs.

---

## Experiments

### 1️⃣ Instruction Following
**File:** `01_instruction_following/clarity_vs_ambiguity.md`

Examines how vague prompts produce inconsistent, difficult-to-evaluate outputs, and how adding structure, scope boundaries, and constraints improves instruction compliance and reduces hallucination risk.

---

### 2️⃣ Prompt Refinement (Multi-Turn Reasoning)
**File:** `02_prompt_refinement/multi_turn_reasoning.md`

Demonstrates how outputs improve across turns as prompts evolve from vague to constrained and measurable.  
This reflects real AI Trainer workflows, where prompts are refined through feedback loops to stabilize quality and evaluability.

---

### 3️⃣ Role / Persona Prompting
**File:** `03_role_persona_prompting/audience_adaptation.md`

Evaluates how models adapt explanations based on audience (layperson vs technical user), focusing on tone control, vocabulary alignment, and preservation of factual accuracy.

---

### 4️⃣ Hallucination Detection (Myth vs Evidence)
**File:** `04_hallucination_detection/myth_vs_evidence.md`

Tests model behavior when handling viral, speculative, or misleading claims, emphasizing:
- separation of myth, speculation, and evidence  
- avoidance of fabricated sources  
- calibrated uncertainty and verification guidance  

---

### 5️⃣ Ambiguous Prompts (Metaphor vs Fact)
**File:** `05_ambiguous_prompts/metaphor_vs_fact.md`

Explores how models handle metaphorical language that is often mistaken for literal scientific claims (e.g., “DNA as an antenna”).  
This category is essential for preventing pseudo-scientific drift while preserving explanatory usefulness.

---

### 6️⃣ Long-Context Reasoning (Consciousness Systems)
**File:** `06_long_context_reasoning/consciousness_systems.md`

Evaluates the model’s ability to:
- retain constraints across extended conversations  
- maintain conceptual consistency  
- enforce boundaries between science, philosophy, and speculation  

This experiment focuses on **long-context failure modes**, where small errors accumulate across turns and lead to subtle misinformation or drift.

---

## Evaluation Framework
**File:** `evaluation_framework.md`

Defines consistent criteria used across all experiments, including:
- instruction compliance  
- factual accuracy  
- hallucination risk  
- uncertainty calibration  
- ambiguity and metaphor handling  
- audience alignment  
- context retention and long-context consistency  
- safety and misinformation awareness  

This framework mirrors how outputs are scored in professional AI evaluation pipelines.

---

## Why This Portfolio Matters
Many real-world AI failures are not caused by direct falsehoods, but by:
- ambiguous requests  
- unsupported inferences  
- misinterpreted metaphors  
- mismatch with user audience  
- drift over extended dialogue  

This repository focuses on **preventing those failure modes**, which is a core responsibility of AI Trainers and Evaluators working on deployed systems.

---

## Author
**Devakrishna Anilkumar**  
Background: Data Science & AI  
Focus: AI evaluation, alignment, and prompt engineering
