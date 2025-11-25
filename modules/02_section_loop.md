## Change Log
- **2025-11-25:** Added `summar_level` variable with conditional behavior.
  - If `summary_level = "short"` → generate compact 1–2 sentence summary.
  - If `summary_level = "detailed"` → generate short paragraph + bullet list of 3–5 key points.
 
# Module 2: Section Loop

## Responsibilities
- **Iterate sections:** Summarize each section according to chosen summary level.
- **Enforce constraints:** Maintain order, terminology, and logical flow.
- **Tailor audience:** Adjust language for expert vs lay readers.

## Inputs
- **Normalized sections:** From Intake & Setup.
- **Audience:** Expert or lay.
- **summary_level:** "short" or "detailed".

## Outputs
- **Per-section summaries:** Labeled, ordered, respecting summary level.
- **Flags:** Missing/empty indicators per section.

## Steps
1. **For each section,** check `summary_level`.
2. **If short:** Write a compact 1–2 sentence summary.
3. **If detailed:** Write a short paragraph (≤150 words) plus a bullet list of 3–5 key points.
4. **Maintain constraints:** Ensure ≤150 words for paragraph, consistent terminology, logical flow.
5. **Attach flags** for missing/empty or <50-word sections when applicable.
