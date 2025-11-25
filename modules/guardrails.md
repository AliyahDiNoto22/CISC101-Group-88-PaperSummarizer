# Module 3: Guardrails

## Responsibilities
- **Missing/empty logic:** Skip summarization; record warnings.
- **Short-section flags:** Mark sections <50 words.
- **Hallucination mitigation:** Restrict content to source text.
- **Long-paper chunking:** Apply context-window strategies.

## Inputs
- **Section data:** Text + length.
- **Chunk metadata:** From Intake & Setup.

## Outputs
- **Warnings list:** Missing/empty, short-section, potential hallucinations.
- **Validated content:** Summaries constrained to source.

## Steps
1. **Validate presence** and minimum length; flag issues.
2. **Cross-check facts** against source sections; avoid invented content.
3. **Chunk and stitch** for long papers; ensure continuity across chunks.
