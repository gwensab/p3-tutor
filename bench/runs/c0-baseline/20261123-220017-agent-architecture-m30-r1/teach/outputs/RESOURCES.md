# Agent architecture Resources

## Knowledge

- [Article: "Effective context engineering for AI agents" (Anthropic Engineering)](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
  Primary guide to keeping an agent's context small and useful. Use for: context rot, notes, runtime retrieval, token-efficient tools.
- [Docs: Context windows (Claude Platform)](https://platform.claude.com/docs/en/build-with-claude/context-windows)
  How the window works and how it is managed. Use for: what counts toward the window, long conversations.
- [Docs: Memory tool (Claude Platform)](https://platform.claude.com/docs/en/agents-and-tools/tool-use/memory-tool)
  File-based memory across conversations, handled by your application. Use for: designing notes between sessions.
- [Paper: "Lost in the Middle: How Language Models Use Long Contexts" (Liu et al.)](https://arxiv.org/abs/2307.03172v1)
  Shows weaker use of information in the middle of long inputs. Use for: arguing against stuffing the context.

## Wisdom (Communities)

- Local: the learner's senior design team and design review.
  Use for: testing the memory design against real questions.
