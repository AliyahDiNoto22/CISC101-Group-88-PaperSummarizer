## Change Log
- **2025-11-25:** Added `evidence_mode = "strict"` to enforce source-only summarization.
- **2025-11-25:** Added standardized warning messages for missing/empty and short sections.

# Module 3: Guardrails

## Responsibilities
- **Missing/empty logic:** Skip summarization; record warnings.
- **Short-section flags:** Mark sections <50 words.
- **Hallucination mitigation:** Restrict content to source text.
- **Long-paper chunking:** Apply context-window strategies.
- **Strict Evidence Mode:** Enforce source-only summarization.

## Inputs
- **Section data:** Text + length.
- **Chunk metadata:** From Intake & Setup.
- **evidence_mode:** "strict" or default.

## Outputs
- **Warnings list:** Missing/empty, short-section, strict evidence notices.
- **Validated content:** Summaries constrained to source.

## Steps
1. **Validate presence** and minimum length.
   - If missing/empty → output: *“Section skipped: no usable text was provided.”*
   - If <50 words → output: *“Section very short: summary may be incomplete.”*
2. **Check evidence_mode.**
   - If `strict`: Only include claims, equations, and results explicitly in source text.
   - If insufficient detail → output: *“The source text does not provide enough detail to summarize this section in strict evidence mode.”*
3. **Cross-check facts** against source sections; avoid invented content.
4. **Chunk and stitch** for long papers; ensure continuity across chunks.
