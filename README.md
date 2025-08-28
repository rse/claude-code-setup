
Claude Code Setup
=================

The [Claude Code](https://www.anthropic.com/claude-code) is a really
awesome and extremely versatile generative AI based tool for
agentic coding support. It ships as a Node.js based command-line interface,
but has built-in integration support for both IDEs like [Visual Studio Code](https://code.visualstudio.com/)
and arbitrary [MCP servers](https://github.com/modelcontextprotocol/servers).
This is [Dr. Ralf S. Engelschall](https://engelschall.com)'s opinionated
setup for Claude Code. If you disagree, just don't use anything from it.

Setup
-----

1. **PREREQUISITE**:

   Install [Node.js](https://nodejs.org) globally into your system 
   and ensure that the `node`, `npm` and `npx` commands are in your `$PATH`.

2. **INSTALL SCRIPT AND CONFIG**:

   Install the content of this repository into your home directory:
  
   ```sh
   $ git clone https://github.com/rse/claude-code-setup
   $ cd claude-code-setup
   $ ./setup install [<prefix>]
   ```

   This installs the `claude` wrapper script into `<prefix>/bin/claude`
   and the configuration files into `<prefix>/.claude/`.

   Notice: the `claude` wrapper script serves four purposes:

   - provide "install" and "update" commands for convenience reasons.
   - pick up and assemble non-standard context files from projects.
   - pick up user and non-project specific system prompt extension.
   - pick up user and non-project specific environment variables.

3. **INSTALL CLAUDE CODE**:

   Install [Claude Code](https://www.anthropic.com/claude-code) and
   the companion tools [TweakCC](https://github.com/Piebald-AI/tweakcc),
   [CCStatusLine](https://github.com/sirmalloc/ccstatusline), and
   [Any-Chat-Completions-MCP](https://github.com/pyroprompts/any-chat-completions-mcp)
   with the help of the `claude` wrapper:

   ```sh
   $ sudo claude install
   ```

   Notice: do not forget to regularily run `sudo claude update` later!

4. [Optional] **SETUP MCP SERVERS**:

   Optionally, and only for the custom `/quorum` command:

   Get API access keys for:

   - OpenAI ChatGPT (directly)
   - Google Gemini  (directly)
   - Deepseek       (directly)
   - xAI Grok       (via OpenRouter)

   Store those access keys in the following environment variables:

   ```
   CLAUDE_CODE_KEY_OPENAI_CHATGPT="..."
   CLAUDE_CODE_KEY_GOOGLE_GEMINI="..."
   CLAUDE_CODE_KEY_DEEPSEEK="..."
   CLAUDE_CODE_KEY_OPENROUTER="..."
   ```

   Then instanciate the corresonding MCP servers (adds entries to `~/.claude.json`):

   ```sh
   claude mcp add --scope user --transport stdio \
       -e AI_CHAT_KEY="$CLAUDE_CODE_KEY_OPENAI_CHATGPT" \
       -e AI_CHAT_NAME="OpenAI ChatGPT" \
       -e AI_CHAT_MODEL="gpt-5" \
       -e AI_CHAT_BASE_URL="https://api.openai.com/v1" \
       -- chat-openai-chatgpt any-chat-completions-mcp
   claude mcp add --scope user --transport stdio \
       -e AI_CHAT_KEY="$CLAUDE_CODE_KEY_GOOGLE_GEMINI" \
       -e AI_CHAT_NAME="Google Gemini" \
       -e AI_CHAT_MODEL="gemini-2.5-flash" \
       -e AI_CHAT_BASE_URL="https://generativelanguage.googleapis.com/v1beta/openai/" \
       -- chat-google-gemini any-chat-completions-mcp
   claude mcp add --scope user --transport stdio \
       -e AI_CHAT_KEY="$CLAUDE_CODE_KEY_DEEPSEEK" \
       -e AI_CHAT_NAME="DeepSeek" \
       -e AI_CHAT_MODEL="deepseek-chat" \
       -e AI_CHAT_BASE_URL="https://api.deepseek.com/v1" \
       -- chat-google-gemini any-chat-completions-mcp
   claude mcp add --scope user --transport stdio \
       -e AI_CHAT_KEY="$CLAUDE_CODE_KEY_OPENROUTER" \
       -e AI_CHAT_NAME="xAI Grok" \
       -e AI_CHAT_MODEL="x-ai/grok-code-fast-1" \
       -e AI_CHAT_BASE_URL="https://openrouter.ai/api/v1" \
       -- chat-xai-grok any-chat-completions-mcp
   ```

5. **GET ACCESS TO CLAUDE CODE**:

   Access to Claude Code:Here you have two options:

   - [Claude Code Free/Pro/Max-5x/Max-20x subscription](https://www.anthropic.com/claude-code#get-started) (recommended)
   - [Anthropic API subscription](https://www.anthropic.com/pricing) (alternatively)

   Notice: the first option provides access to Anthrophic Claude only
   via Web interfaces and to the API only indirectly via Claude Code, while
   only the second option also allows direct access to the Anthropic Claude API.

   Notice: the first option is best for Claude Code because it has less limits
   and is more cost effective. The second option is more versatile, as you
   can use this subcription for more than just Claude Code.

6. **LOGIN TO CLAUDE CODE**:

   Login to [Claude Code](https://www.anthropic.com/claude-code):

   ```
   $ claude
   /login
   ```

