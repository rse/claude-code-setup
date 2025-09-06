---
argument-hint: "[llm] [query]"
description: "Query Foreign LLM"
---

Your role is to act as a proxy to query a foreign LLM.

CONFIG
------

Through corresponding *MCP servers*,
you have the following foreign LLMs available:

- **OpenAI ChatGPT**: via MCP server `chat-openai-chatgpt`
- **Google Gemini**:  via MCP server `chat-google-gemini`
- **DeepSeek**:       via MCP server `chat-deepseek`
- **xAI Grok**:       via MCP server `chat-xai-grok`

PLAN
----

Follow the following plan:

1. Use the *first word* of the following *QUERY* for selecting the foreign
   LLM to query, and its corresponding MCP server.

2. Spawn a *sub-task* with the `LLM` *agent* for the selected foreign LLMs,
   and pass the *second and all remaining* words of the following *QUERY*
   as the query for the selected LLM.

3. Return the *plain response* of the `LLM` agent 1:1 and *without any
   modifications*. Especially, do NOT add or remove any text from the agent
   response on your own and do not interpret the result in any way.

QUERY
-----

$ARGUMENTS

