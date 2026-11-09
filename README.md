# Australia Legal Research MCP Server (`au-legal-mcp`)

## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Australia (AU)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Australia**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | Federal Circuit and Family Court, State District/County & Magistrates/Local Courts (NSW, VIC, QLD, WA, SA, TAS, ACT, NT) |
| **Tier 2 — Regional / Cantonal / Appellate** | Federal Court of Australia (FCA / FCAFC) & State/Territory Supreme Courts and Courts of Appeal (NSWCA, VSCA, QCA, WASCA, SASCA) |
| **Tier 3 — Supreme & Constitutional** | High Court of Australia (HCA) |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** Federal Register of Legislation (legislation.gov.au) & AustLII — [https://www.legislation.gov.au](https://www.legislation.gov.au)
  - *Indexed Legislation Domains:* `legislation.gov.au`, `austlii.edu.au`
- **Court Decisions & Jurisprudence Archives:** AustLII & State/Federal Caselaw Portals (caselaw.nsw.gov.au / fedcourt.gov.au / hcourt.gov.au) — [https://www.caselaw.nsw.gov.au](https://www.caselaw.nsw.gov.au)
  - *Indexed Judicial & Open Case Law Domains:* `austlii.edu.au`, `caselaw.nsw.gov.au`, `fedcourt.gov.au`, `hcourt.gov.au`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Australia. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Australia. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Australia. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "au-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/au-legal-mcp/archive/refs/heads/main.zip",
        "au-legal-mcp"
      ]
    }
  }
}
```
</details>
