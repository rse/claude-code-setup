---
argument-hint: "[question]"
description: "Query Multiple AIs for Quorum Answer"
---

<execute>
@~/.claude/commands/meta/prolog.md
</execute>

<command>
Query Multiple AIs for Quorum Answer
</command>

<role>
Your role is an expert-level assistant.
</role>

<objective>
Find a quorum answer on an arbitrary question,
by querying multiple AIs for an optimal consensus.
</objective>

PLAN
----

Closely follow the following *<plan/>* of distinct *<task/>*,
in the given chronological order:

<plan>
1. <task id="ANSWER">Determine your own answer.</task>
2. <task id="PREVIEW">Show your own answer as a sneak preview.</task>
3. <task id="QUERY">For additional answers, query multiple AIs via *sub-tasks* and the `LLM` *agent*.</task>
4. <task id="SUMMARY">Determine a summary of all answers in total.</task>
5. <task id="RATING">Determine a consensus rating of all answers.</task>
6. <task id="OUTPUT">Give a consolidated output.</task>
</plan>

EXECUTION
---------

For yourself (Anthropic Claude), first answer the following *<query/>* in advance:

<query>
$ARGUMENTS.
Please respond with facts and very concise and brief only,
usually with just 1 to 7 corresponding bullet points and with short sentences.
Optionally, mention potential cruxes which should be noticed.
Beside bullet points, do not provide any additional explanations.
Emphasize keywords or cruxes in your response with Markdown formatting.
Format code parts with Markdown formatting.
</query>

Then show your results based on the following outout <template/>:

<template>
**Anthropic Claude** (sneak preview in advance):
- [...]
- [...]
</template>

Then, for each of the following foreign AIs and their given corresponding MCP servers,
use a *sub-task* and the `LLM` *agent* to perform the above same *<query/>* again:

- OpenAI ChatGPT: `chat-openai-chatgpt`
- Google Gemini:  `chat-google-gemini`
- DeepSeek:       `chat-deepseek`
- xAI Grok:       `chat-xai-grok`

Then:

1. Summarize all responses, of both yourself and all MCP servers,
   with just 1 to 7 corresponding bullet points and with short sentences.
2. Determine, on a Likert scale of 0..5, the amount of the overall
   consensus of all the responses.

OUTPUT
------

Finally show the summary, the consensus and the complete and unmodified responses
of yourself and each of the MCP servers, based on the following output <template/>:

<template>
**QUESTION**:
$ARGUMENTS

&#x25CF; **CONSENSUS ANSWER**:
- [...]
- [...]

**CONSENSUS RATE**: [...]

&#x25CB; **Anthropic Claude**:
- [...]
- [...]

&#x25CB; **OpenAI ChatGPT**:
- [...]
- [...]

&#x25CB; **Google Gemini**:
- [...]
- [...]

&#x25CB; **DeepSeek**:
- [...]
- [...]

&#x25CB; **xAI Grok**:
- [...]
- [...]
</template>

