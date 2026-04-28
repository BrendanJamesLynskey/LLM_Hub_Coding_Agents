# Coding Agents Internals

How Cursor, Aider, Claude Code and Codex CLI understand a repository, manage context, use tools, and delegate work &mdash; the heuristics, the diff formats, the cache mechanics and the architectural differences.

**Live index:** https://brendanjameslynskey.github.io/LLM_Hub_Coding_Agents/

## Presentations in this series

### Foundations &mdash; how the agent reads and edits

| # | Title | Status | Description |
|---|-------|--------|-------------|
| 01 | [Repo Understanding](https://brendanjameslynskey.github.io/CodingAgents_01_Repo_Understanding/) | live | ripgrep heuristics that beat embeddings; tree-sitter ASTs; ctags &amp; LSPs; code embeddings (when they help, when they don't); dependency graphs; Aider repo map, Cursor @-references, Claude Code heuristics. |
| 02 | [Edit Strategies](https://brendanjameslynskey.github.io/CodingAgents_02_Edit_Strategies/) | live | Search-replace, unified diff, patch files; multi-file atomicity; context window management; Read/Edit/Write tool design; Aider vs Cursor vs Claude Code architectures; failure recovery. |

### Companion to Sebastian Raschka &mdash; *Components of a Coding Agent*

A five-deck companion to [Sebastian Raschka's essay](https://magazine.sebastianraschka.com/p/components-of-a-coding-agent), unpacking each of the six components &mdash; live repo context, prompt-cache reuse, tool access, context bloat, structured session memory, bounded subagents &mdash; with diagrams, code, and interactive visualisations. Read alongside the article.

| # | Title | Status | Description |
|---|-------|--------|-------------|
| 03 | [Components Overview](https://brendanjameslynskey.github.io/CodingAgents_03_Raschka_Components_Overview/) | live | The harness mental model; LLM vs reasoning model vs agent; the four-step `observe → inspect → choose → act` loop; the six-component architecture; why the harness can outweigh the model. |
| 04 | [Repo Context &amp; Prompt Cache](https://brendanjameslynskey.github.io/CodingAgents_04_Raschka_Repo_Context_And_Caching/) | live | Components 1 + 2. Workspace summaries; stable-vs-changing prefix; Anthropic 5-min TTL cache mechanics (1.25× write, 0.10× read); interactive cache-cost calculator; CLAUDE.md / AGENTS.md patterns. |
| 05 | [Tool Access &amp; Use](https://brendanjameslynskey.github.io/CodingAgents_05_Raschka_Tool_Use/) | live | Component 3. Prose vs bounded actions; tool-call anatomy; the four validation gates; approval modes; tool taxonomy; schema design; interactive approval-gate simulator with adversarial inputs. |
| 06 | [Context Bloat &amp; Session Memory](https://brendanjameslynskey.github.io/CodingAgents_06_Raschka_Context_Bloat_And_Memory/) | live | Components 4 + 5. Clipping, dedup, recency-weighted summarisation; working memory vs full transcript; storage-time vs prompt-time discipline; live context-budget visualiser. |
| 07 | [Subagents &amp; Synthesis](https://brendanjameslynskey.github.io/CodingAgents_07_Raschka_Subagents_And_Synthesis/) | live | Component 6 + closing synthesis. Spawn vs bind; sandboxing and recursion depth; Claude Code vs Codex models; pattern catalogue (research / parallel-edit / review / autonomous slice / planner-executor); interactive subagent-tree explorer; reading list. |

## Where this fits

Part of the [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs) &mdash; an index of presentation series for AI/LLM engineers.
