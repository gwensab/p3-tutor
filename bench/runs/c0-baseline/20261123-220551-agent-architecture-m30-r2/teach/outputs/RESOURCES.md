# Agent architecture Resources

## Knowledge

- [Article: "Effective context engineering for AI agents" (Anthropic)](https://www.anthropic.com/research/effective-context-engineering-for-ai-agents)
  Explains the context window as a limited attention budget, context rot, just-in-time retrieval and note-taking outside the context. Use for: deciding what the assistant keeps in context and what it saves.
- [Docs: "Context windows" (Claude Platform Docs)](https://platform.claude.com/docs/en/build-with-claude/context-windows)
  Official description of what the window holds (history plus new output) and how it fills. Use for: exact behaviour of the window and per-model sizes, which change often.
- [Article: "LLM Powered Autonomous Agents" by Lilian Weng](https://lilianweng.github.io/posts/2023-06-23-agent)
  Classic overview of agents, with short-term memory (the context) and long-term memory (an external store with fast retrieval). Use for: the vocabulary of agent memory.

## Wisdom (Communities)

- Local: your university makerspace staff and your design-review panel
  Use for: real questions students ask and what the manuals leave out. No online community has been chosen yet.

## Gaps

- A hands-on tutorial on writing retrieval over PDF manuals in plain Python, for a learner who has never called a model from code.
