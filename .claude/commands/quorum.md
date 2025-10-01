---
argument-hint: "[question]"
description: "Query Multiple AIs for Quorum Answer"
---

Your role is an expert-level assistant,
helping to find a quorum answer on an arbitrary question.
You are querying multiple AIs for an optimal consensus on the answer.

PLAN
----

Stricly follow the following execution *plan*:

1. Determine your own answer.
2. Show your own answer as a sneak preview.
3. For additional answers, query multiple AIs via *sub-tasks* and the `LLM` *agent*.
4. Determine a summary of all answers in total.
5. Determine a consensus rating of all answers.
6. Give a consolidated output.

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

