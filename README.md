# Cognitive Investment Engine (LLM Equity Wiki)

A local, AI-powered knowledge graph and autonomous equity research assistant, heavily inspired by Andrej Karpathy's "LLM OS" concept. 

This project uses the Gemini CLI as the reasoning engine ("CPU"), local Markdown files as the knowledge base ("Memory"), and Obsidian.md as the visual interface to map out complex supply chains and second-order financial impacts.

## The Concept
Traditional financial tracking relies on static spreadsheets and isolated PDFs. This system transforms raw financial documents (10-Ks, Earnings Transcripts, News) into a living, interconnected graph. 

When a new document is ingested, the AI doesn't just summarize it; it updates the company's historical financial tables, maps out newly discovered suppliers/customers, and crawls the ecosystem to adjust its investment thesis based on network effects.

## Tech Stack
* Gemini CLI: The autonomous reasoning and execution agent.
* Obsidian.md: Renders the local markdown files into an interactive node graph.
* Markdown: The universal, future-proof storage format for the data.
* PowerShell/Git: Local execution and version control of the AI's reasoning over time.

## Core Features

### 1. Autonomous Data Ingestion
Drop a raw PDF or TXT file (e.g., an Annual Report or News Article) into the vault and tell the CLI to execute the workflow. The AI will automatically rename the file to a strict naming convention, move it to the correct ticker folder, and extract the relevant data.

### 2. The Ecosystem Graph (Supply Chain Mapping)
The AI is strictly prompted to wrap any mentioned publicly traded companies in Obsidian wikilinks (e.g., [[AAPL]], [[NVDA]]). This automatically builds a visual dependency graph showing exactly who supplies whom, allowing for immediate visualization of single points of failure in the market.

### 3. Time-Series Tracking (Guidance vs. Actuals)
Every company maintains a _master_profile.md. As quarterly earnings are ingested, the AI appends data to a "Continuing Financials" table, keeping a permanent record of management's past guidance versus their actual performance to assess credibility.

### 4. Second-Order AI Synthesis
When a catalyst occurs (e.g., a supplier announces a production delay), the AI performs an "Ecosystem Crawl." It checks the profiles of linked customers and updates their profiles with warnings, synthesizing a new "AI Opinion" based on the blast radius of the news.

## Vault Structure

```text
my-stock-wiki/
├── GEMINI.md                    # The "System Prompt" / Autonomous Operating System
├── Investment_Ideas.md          # Auto-generated reports on "Hidden Backbone" stocks
├── AAPL/
│   ├── AAPL_master_profile.md   # The living identity, financials, and AI Opinion
│   ├── AAPL_2026_Q1_Earnings.md # Processed transcript
│   └── AAPL_2025_10K.md         # Processed annual report
├── TSM/
│   ├── TSM_master_profile.md
│   └── TSM_2026-04-22_News_Factory_Update.md
└── index.md                     # Portfolio dashboard
