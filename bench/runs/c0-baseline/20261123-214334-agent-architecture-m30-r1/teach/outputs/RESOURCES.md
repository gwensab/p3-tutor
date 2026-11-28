# Agent architecture Resources

## Knowledge

- [Article: "Effective context engineering for AI agents" (Anthropic Engineering)](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
  Context, context rot, compaction, note-taking, just-in-time retrieval. Use for: what to keep in context and when to shrink or save it.
- [Docs: Context windows (Claude Platform)](https://platform.claude.com/docs/en/build-with-claude/context-windows)
  What counts toward the window, overflow behavior, history re-sent each turn. Use for: token counting and cost.
- [Docs: Memory tool (Claude Platform)](https://platform.claude.com/docs/en/agents-and-tools/tool-use/memory-tool)
  How a model reads and writes memory files while the application runs the operations. Use for: designing memory between sessions.
- [Guide: RAG chunking phase (Microsoft Azure Architecture Center)](https://learn.microsoft.com/azure/architecture/ai-ml/guide/rag/rag-chunking-phase)
  Practical chunking choices. Use for: splitting manuals for search.
- [Survey: Retrieval-Augmented Generation for Natural Language Processing (arXiv 2407.13193)](https://arxiv.org/pdf/2407.13193)
  Overview of chunking, embedding, ranking and generation. Use for: background on the retrieval pipeline.

## Gaps

- A trusted community for agent builders; none verified yet.
