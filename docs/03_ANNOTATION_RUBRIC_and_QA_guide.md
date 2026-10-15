# Project 01 v2 — Rubric scoring and quality-control guide

## Goal
Independently score each AI response against its task-specific fictional policy. No real customer data or company is involved.

## Four rubric criteria, each rated 1–5

The four criteria are **factual accuracy**, **relevance**, **completeness**, and **clarity**. The numbers 1 through 5 are **rating values**, not additional criteria.

| Score | Factual accuracy | Relevance | Completeness | Clarity |
|---|---|---|---|---|
| 1 | Directly contradicts a decisive policy | Does not answer the question | Omits essential answer | Incomprehensible or misleading wording |
| 2 | Several errors or one consequential error with some true content | Mostly off-target | Severe missing information | Difficult to follow |
| 3 | Approximate/partially supported, no major harmful guarantee | Partly answers | Provides some important steps, misses several | Understandable but vague |
| 4 | Accurate with slight imprecision | Largely on point | Mostly sufficient, omits a useful detail | Clear with minor weakness |
| 5 | Supported by relevant reference facts, no known contradictions | Directly answers | Covers key details needed for the question | Precise, easy to act on |

## Overall rating
The **overall quality score** is a separate rating, **not a fifth evaluation criterion**. Use the same 1–5 quality scale but make a **holistic judgement**; do not mechanically average dimension ratings. A severe policy contradiction or fabricated guarantee normally caps the overall score at **1 or 2** even if language is clear. If a response only names the city instead of a complete office address, accuracy may be 5 but completeness lower and overall 4.

## Evidence verdict
- **Supported:** Every material factual claim is supported by task-specific policy context. (The answer may still be incomplete.)
- **Contradicted:** At least one material factual claim conflicts with a policy.
- **Insufficient evidence:** The reference does not support or refute a material claim; do not invent missing facts.

## Example: RUB-006
- Customer asks "Where is your office?" AI gives "headquartered in Enugu".
- P05 supplies a full fictional Enugu street address. Factual accuracy = 5; completeness = 3; suggested overall = 4.
- This is a **judgement-based benchmark**, not an objective numeric measurement.

## Example: RUB-007
- AI says **support@northstarhome.example**.
- P04 says only **care@northstarhome.example** is official.
- Verdict = contradicted, wrong contact, suggested low factual accuracy.
- `.example` is a reserved nonfunctional domain. Never send emails to it.

## Reviewer protocol
1. Read the customer prompt and AI response in Label Studio.
2. Read the task's reference context and policy IDs; the policy is authoritative only for this exercise.
3. Rate the **four rubric criteria** (factual accuracy, relevance, completeness, and clarity), then assign a **separate overall quality score**. All five ratings use the 1–5 scale.
4. Select factual-evidence verdict and any applicable issue tags.
5. In your justification, explicitly refer to policy IDs and relevant differences.
6. Optionally write a corrected response.
7. Submit and move to the next record. Keep the private answer key unopened until all cases are complete.
8. Export annotations to JSON or CSV, map by `record_id`, compare against the private benchmark, and analyze disagreements. Repeated cases from the original 30 have been replaced with new scenarios.

## Portfolio integrity
- State that all 30 cases and policies are **synthetic**.
- Explain how reference facts were authored and how the labels were evaluated.
- Human benchmark ratings are illustrative and may reasonably differ by one point; document decisions, not only agreement percentages.
- Do not claim that the fictional email or street address corresponds to a real business.
