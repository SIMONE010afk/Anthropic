<h1 align="center">
  <img src="assets/anthropic-animated.svg" alt="Anthropic" width="560" />
</h1>

Collection of exercises and prototypes built during the "Building with the Claude API" course. The repository is organized by module, with notebooks and small projects that showcase different capabilities.

## Quick Map

| Folder | Focus |
| --- | --- |
| `App_starter/` | **Starter MCP toolkit** (FastMCP server + example tools + tests) |
| `MCP/` | **CLI MCP chat app** (local doc server, tools, prompts, autocomplete) |
| `Prompting/` | **Prompt evaluation lab** (dataset generation + scoring + HTML report) |
| `RAG/` | **RAG pipeline playground** (chunking, embeddings, BM25, reranking, hybrid) |
| `Tools/` | **Tooling showcase** (caching, code execution, web search, multimodal, streaming) |

## Folder Highlights

<details>
<summary><strong>App_starter</strong> - Starter MCP toolkit</summary>

- FastMCP server in `main.py` registering tools.
- Example tools: numeric `add` and binary document -> markdown conversion.
- Basic tests for DOCX/PDF fixtures.
- Key deps: `mcp[cli]`, `markitdown[docx,pdf]`, `pydantic`, `pytest`.

</details>

<details>
<summary><strong>MCP</strong> - CLI MCP chat app</summary>

- `cli_project/` runs the MCP client and an interactive CLI with autocomplete.
- `mcp_server.py` exposes resources, tools, and prompts over sample docs.
- Handles tool calls, prompts, and document references via `@doc`.
- Key deps: `anthropic`, `mcp[cli]`, `prompt-toolkit`, `python-dotenv`.

</details>

<details>
<summary><strong>Prompting</strong> - Prompt evaluation lab</summary>

- Notebook for prompt testing end-to-end.
- `PromptEvaluator` builds test sets, grades outputs, and exports HTML reports.
- Example evaluation scenario included.

</details>

<details>
<summary><strong>RAG</strong> - RAG pipeline playground</summary>

- Multiple chunking strategies (size, sentence, section).
- Lexical BM25 search + semantic embedding retrieval.
- Vector indexing, reranking, and hybrid RRF workflows.
- Shared corpus in `Chunk_text/report.md`.

</details>

<details>
<summary><strong>Tools</strong> - Tooling showcase</summary>

- Caching, code execution, and text editor tool patterns.
- Web search with domain restrictions.
- Multimodal examples (images/PDF) and tool streaming.
- Support assets (CSV, images, PDF).

</details>
