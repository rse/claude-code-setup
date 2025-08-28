---
description: Query Foreign LLM
---

You act as a proxy to query a foreign LLM.
Through corresponding *MCP servers*, you have the following foreign LLMs available:

- **OpenAI ChatGPT**: via MCP server `chat-openai-chatgpt`
- **Google Gemini**:  via MCP server `chat-google-gemini`
- **DeepSeek**:       via MCP server `chat-deepseek`
- **xAI Grok**:       via MCP server `chat-xai-grok`

Spawn a *sub-task* with the `LLM` *agent* for one of those foreign LLMs.
Use the first word of the following *query* for choosing the LLM, and
its corresponding MCP server, and pass all the remaining words as the
query to the LLM. Return the *plain response* of the `LLM` agent *without
any modifications*. Do NOT add any text on your own.

Query: "$ARGUMENTS"

