# Final Label Studio export validation

**Source:** Label Studio exports `northstar_ai_evaluation_completed(4).json` and `northstar_ai_evaluation_completed(4).csv`, supplied on 15 October 2026. Exact copies are stored in `annotations/` under standardized filenames. Original scores, issue tags, verdicts, and justifications are not modified for publication.

## Verified checks

- **30/30 unique record IDs:** `RUB-001` through `RUB-030`, each with exactly one submitted annotation.
- **30/30 complete annotations:** four 1–5 criterion scores, separate overall score, evidence verdict, and a nonempty written justification.
- **30/30 overall scores match the score at the beginning of the written justification.**
- **0 JSON/CSV semantic discrepancies:** original files match after normalizing Label Studio’s CSV encoding of multi-select tags and newline styles.
- **0 task-data discrepancies:** prompts, AI responses, reference policy text, and identifiers match the unlabeled dataset.
- **19 Supported · 11 Contradicted · 0 Insufficient evidence.** Overall score counts: 1→10, 2→1, 3→2, 4→3, 5→14.
- The reviewer-friendly CSV and descriptive summary JSON were **regenerated from these same exact annotations**.

## Previously identified corrections — verified in this export

| Record | Verification |
|:---|:---|
| **RUB-003** | The written justification cites what the AI actually said: “all items can be returned at any time.” |
| **RUB-006** | Factual-evidence verdict changed to **Supported**, consistent with policy P05. |
| **RUB-008** | The justification now correctly quotes **“within 30 days of delivery”**, as written in the AI response. |
| **RUB-010** | The 48-hour requirement is correctly identified as the **damage-reporting deadline**, rather than a normal return period. |
| **RUB-016** | Overall quality rating and justification both state **3/5**. |

## Optional non-blocking refinements

- **RUB-004:** The justification quotes “Monday–Friday” as shorthand for the response’s “Monday to Friday.” Meaning and evaluation are aligned; only character-for-character quoting differs.
- **RUB-026 and RUB-029:** Problem-tag selections are blank, but these are optional fields. Their evidence verdicts, scores, and explanations are present and consistent.

## Interpretation safeguards

The exercise uses **synthetic cases and policy text** and **one human annotator**. The scores are descriptive annotation outcomes, not the accuracy rate of a production AI system, inter-annotator agreement, or measured business impact. No private benchmark answer key or benchmark statistics are included in the public project package.
