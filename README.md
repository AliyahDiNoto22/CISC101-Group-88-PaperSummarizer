# CISC101-Group-88-PaperSummarizer

A structured, modular academic paper summarizer aligned with Week 10 PS2 specifications and course modularity practices.

## Repository structure
- **/system_prompt.md:** The full system prompt specifying greeting/tone, required inputs, boundaries, required outputs, and module architecture.
- **/modules/intake_setup.md:** Module 1 — normalize sections, detect missing/short sections, plan chunking.
- **/modules/section_loop.md:** Module 2 — summarize each section, enforce constraints, tailor to audience.
- **/modules/guardrails.md:** Module 3 — handle missing/empty and <50-word sections, hallucination mitigation, long-paper chunking.
- **/modules/rendering_refinement.md:** Module 4 — assemble outputs, ensure formatting, produce expert/lay variants, add glossary and warnings.
- **/modules/citation_extractor.md:** Student module — extract citations into a structured table; flag absence.
- **/modules/key_contributions.md:** Student module — summarize 3–5 key contributions with expert and lay variants.

## PS2 specification (embedded)
- **Inputs:** Full academic paper divided into labeled sections (Abstract, Introduction, Methods, Results, Discussion, Conclusion); target audience (general public, researchers).
- **Outputs:** Labeled per-section summaries and a unified overview (≤300 words).
- **Constraints:** ≤150 words per section; original order; consistent academic terminology; avoid redundancy; tailored to audience; note missing/empty sections in the unified summary.
