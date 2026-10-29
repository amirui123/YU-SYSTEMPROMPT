# GitHub research inventory (2026-10-29)

Ten separate topic searches were run using GitHub-restricted web queries. Each returned a maximum of ten results and all returned entries were reviewed (100 result entries total; this is not equivalent to exhaustive GitHub index coverage). Search dimensions: leaked/system prompt collections; frameworks; agent prompts; prompt management; evaluation; DSPy optimization; multi-agent/tool-use; RAG/memory; persona/tone; awesome lists. Search output was from web search (not GitHub's authenticated UI).

The 15 candidates are documented individually in `items/`. Metadata (stars, updated_at, pushed_at, license) was queried from the public GitHub REST API on 2026-10-29. README pages/tree and/or search-result README excerpts were read for design patterns. Nine license-verified repositories were shallow/sparse cloned under `repos/`; this is research material, not product code. See each note for limits of evidence.

## Inventory

| Repo | Stars | Updated/pushed | License | Main takeaway | Recommendation |
|---|---:|---|---|---|---|
| [microsoft/PromptKit](items/microsoft-PromptKit.md) | 113 | 2026-10-21 / push 2026-10-28 | MIT | Composable prompt library: personas, protocols, formats, taxonomies, task templates; versioned and layered | adapt idea |
| [promptfoo/promptfoo](items/promptfoo.md) | 26,567 | 2026-10-29 / push 2026-10-29 | MIT | Evaluation/red-team framework for prompts, agents and RAG | adapt idea |
| [stanfordnlp/dspy](items/dspy.md) | 38,842 | 2026-10-29 / push 2026-10-28 | MIT | Programmatic LM framework: typed signatures/modules separate task contract from implementation; optimizers compile against examples/metrics | adapt idea |
| [langchain-ai/langgraph](items/langgraph.md) | 44,073 | 2026-10-29 / push 2026-10-28 | MIT | Stateful agent orchestration using graphs, nodes, edges, persistence and human-in-loop patterns | adapt idea |
| [dair-ai/Prompt-Engineering-Guide](items/Prompt-Engineering-Guide.md) | 79,631 | 2026-10-29 / push 2026-03-11 | MIT | Large tutorial/resource guide spanning techniques, papers, RAG, context and agents | adapt idea |
| [danielmiessler/fabric](items/fabric.md) | 44,484 | 2026-10-29 / push 2026-10-26 | MIT | Reusable task-specific prompt patterns wrapped in CLI workflows; illustrates composable task modules and human-readable pattern files | adapt idea |
| [openai/openai-cookbook](items/openai-cookbook.md) | 76,860 | 2026-10-29 / push 2026-10-29 | MIT | Official API examples, evaluation and production workflows | adapt idea |
| [google-gemini/cookbook](items/google-gemini-cookbook.md) | 17,876 | 2026-10-29 / push 2026-10-27 | Apache-2.0 | Official Gemini API examples with grounding, multimodal, structured outputs and API usage | adapt idea |
| [anthropics/prompt-eng-interactive-tutorial](items/anthropic-prompt-tutorial.md) | 38,904 | API updated 2026-10-29 / push 2026-08-28 | NO LICENSE DECLARED | Official interactive tutorial, guided examples for Claude prompt construction | ideas only; no copying |
| [anthropics/courses](items/anthropic-courses.md) | 22,942 | API updated 2026-10-29 / push 2026-08-28 | NOASSERTION | Official educational notebooks/courseware for Claude use and evaluation | ideas only; no copying |
| [Piebald-AI/claude-code-system-prompts](items/claude-code-system-prompts.md) | 13,021 | 2026-10-29 / push 2026-10-27 | MIT (repository) | Versioned snapshots of coding-agent prompt components, tools and specialist subagents | ideas only; no copying |
| [asgeirtj/system_prompts_leaks](items/system-prompts-leaks.md) | 70,384 | 2026-10-29 / push 2026-10-27 | CC0-1.0 (repository metadata) | Community-maintained collection of extracted vendor system prompts | ideas only; no copying |
| [f/prompts.chat](items/prompts-chat.md) | 174,981 | 2026-10-29 / push 2026-10-29 | NOASSERTION | Large community prompt library | ideas only; no copying |
| [langfuse/langfuse](items/langfuse.md) | 36,671 | 2026-10-29 / push 2026-10-29 | NOASSERTION (API) | Observability, prompt versioning, traces and evaluation; useful production lifecycle concept: version → run → inspect → improve | ideas only; no copying |
| [TrustAI-laboratory/learn-prompt-hacking](items/learn-prompt-hacking.md) | 392 | 2026-10-26 / push 2025-04-12 | MIT | Educational prompt-injection/red-team resource | adapt idea |

## License handling

Cloned only repositories whose GitHub metadata stated MIT/Apache-2.0: PromptKit, promptfoo, DSPy, LangGraph, DAIR Prompt Engineering Guide, Fabric, OpenAI Cookbook, Google Gemini Cookbook, and TrustAI prompt-hacking course. Their contents remain in their original repositories under `repos/`; no third-party prompt text has been copied into the final system prompt. Repository-level license data is not treated as a license for vendor prompt content pasted into a repository. Sources with absent/NOASSERTION license are excluded from verbatim reuse.

## Directories

- `repos/`: nine shallow/sparse clones of license-verified repositories.
- `items/`: one verification and assessment note per candidate (15 total).
