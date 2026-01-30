# Anthropic

Raccolta di esercizi e prototipi legati al corso "Building with the Claude API". Il repository e organizzato per moduli (App starter, MCP, Prompting, RAG, Tools) con notebook e piccoli progetti di esempio.

## Struttura rapida

| Cartella | Scopo |
| --- | --- |
| `App_starter/` | Template MCP minimale con tool di esempio e test |
| `MCP/` | CLI chat con server MCP locale (documenti, tool, prompt) |
| `Prompting/` | Notebook per valutazione e testing di prompt |
| `RAG/` | Pipeline RAG: chunking, embedding, retrieval, reranking |
| `Tools/` | Esempi tool Anthropic (caching, code exec, web search, multimodale, streaming) |

## Dettagli per cartella

<details>
<summary><strong>App_starter</strong> - template MCP minimale</summary>

- Server FastMCP in `main.py` che registra tool.
- Tool `add` e conversione documenti binari -> markdown con `markitdown`.
- Test base su fixture docx/pdf.
- Dipendenze: `mcp[cli]`, `markitdown[docx,pdf]`, `pydantic`, `pytest`.

</details>

<details>
<summary><strong>MCP</strong> - progetto CLI chat</summary>

- `cli_project/` avvia un client MCP e una CLI con autocomplete.
- `mcp_server.py` espone risorse, tool e prompt su un set di documenti fittizi.
- Gestione di tool use, prompt e risorse (anche con riferimenti `@doc`).
- Dipendenze: `anthropic`, `mcp[cli]`, `prompt-toolkit`, `python-dotenv`.

</details>

<details>
<summary><strong>Prompting</strong> - valutazione prompt</summary>

- Notebook completo per generare dataset di test e valutare prompt.
- Classe `PromptEvaluator` con generazione idee, casi di test e grading.
- Report finale in HTML con statistiche e tabella risultati.

</details>

<details>
<summary><strong>RAG</strong> - retrieval-augmented generation</summary>

- Chunking per dimensione, frasi e sezioni (`Chunk_text/`).
- Ricerca lessicale BM25 e ricerca semantica con embedding.
- Vector index, reranking, e approccio ibrido (RRF).
- Esempi su un corpus unico (`Chunk_text/report.md`).

</details>

<details>
<summary><strong>Tools</strong> - tool Anthropic in pratica</summary>

- Caching, code execution, text editor tool, thinking.
- Web search con domini consentiti.
- Input multimodale (immagini, PDF) e tool streaming.
- Asset di supporto: CSV, immagini, PDF.

</details>
