# Agent Architecture Resources

## Knowledge

- [Article: "Effective context engineering for AI agents" (Anthropic)](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
  Primary source for O3. Use for: context rot, tool result clearing, compaction, note-taking, just-in-time retrieval.
- [Docs: Context windows](https://platform.claude.com/docs/en/build-with-claude/context-windows)
  Use for: what counts toward the window, overflow behavior, caching and billing.
- [Docs: Working with messages](https://platform.claude.com/docs/en/build-with-claude/working-with-messages)
  Use for: stateless calls and resending conversation history.
- [Docs: Conversation state](https://developers.openai.com/api/docs/guides/conversation-state)
  Seen through search results only. Use for: billing when the service stores history.
- [Docs: Memory overview (LangChain)](https://docs.langchain.com/oss/python/concepts/memory)
  Use for: short-term and long-term memory, profiles and collections, when to write memories.
- [Article: "Contextual Retrieval" (Anthropic)](https://www.anthropic.com/engineering/contextual-retrieval)
  Use for: RAG steps, chunking, embeddings and BM25, when to include a whole knowledge base.
- [Docs: Tokens (Google)](https://ai.google.dev/gemini-api/docs/tokens)
  Use for: what a token is and rough size estimates.

## Wisdom (Communities)

- [LangChain forum](https://forum.langchain.com/)
  Has a "Talking Shop" category for agent design. Use for: feedback on memory and retrieval choices.
