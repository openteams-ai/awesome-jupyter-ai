# Awesome Jupyter AI [![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

> AI extensions for JupyterLab and Jupyter Notebook 7 | [Blog post](https://openteams.com/awesome-jupyter-ai-extensions/)

We are excited to see the Jupyter extension ecosystem thrive in the era of AI. The variety of ideas and implementations demonstrates the utility of the extension platform and the API stability offered by JupyterLab. This list collects over a hundred AI extensions for JupyterLab and Jupyter Notebook 7. They range from chat panels and inline completers to teaching tools and the building blocks of Jupyter AI. Each one installs into a JupyterLab or Notebook 7 you already run.

The authors include individuals, universities, research institutes and corporations. Listing an extension here is not an endorsement.

## Contents

- [How this list is organised](#how-this-list-is-organised)
- [At a glance](#at-a-glance)
- [Chat panels and agents](#chat-panels-and-agents)
- [Inline completion](#inline-completion)
- [In-cell edits and magics](#in-cell-edits-and-magics)
- [Agent CLI bridges](#agent-cli-bridges)
- [Domain, teaching and platform](#domain-teaching-and-platform)
- [Building blocks](#building-blocks)
  - [Jupyter AI plugins](#jupyter-ai-plugins)
  - [Chat and notebook UI](#chat-and-notebook-ui)
  - [Live reload](#live-reload)
  - [MCP](#mcp)
- [Beyond the JupyterLab UI](#beyond-the-jupyterlab-ui)

## How this list is organised

Sections group the extensions by what they do. Inside a section, each entry has a marker for how recently the project was worked on:

| Marker | Name | Last commit |
| --- | --- | --- |
| 🟢 | active | Within 4 months |
| 🟡 | maintained | Within 12 months |
| ⚪ | quiet | 1 to 2 years ago |

Anything older lives in [HISTORICAL.md](HISTORICAL.md), together with the archived projects and the ones whose model service has been switched off. The date is derived from the last commit on the default branch, or the latest PyPI release when there is no public repository.

<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> marks a project maintained by [Project Jupyter](https://jupyter.org/governance/list_of_subprojects.html), in one of its official GitHub organisations.

🪐 marks a project in [jupyter-ai-contrib](https://github.com/jupyter-ai-contrib), the community organisation where Jupyter AI v3 is built as separate packages. It is not under Project Jupyter governance.

Star counts in the table are for orientation only. Read the licence before you depend on an extension: Notebook Intelligence is GPL-3.0, and several entries have an open licence but no public repository.

## At a glance

This lists major projects, but each has a few alternatives listed in sections below. 

| Project | What it adds | Stars | Last commit | License |
| --- | --- | --- | --- | --- |
| <img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="12" alt="Project Jupyter"> [Jupyter AI](https://github.com/jupyterlab/jupyter-ai) | Chat with external agents over ACP | ![](https://img.shields.io/github/stars/jupyterlab/jupyter-ai?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/jupyterlab/jupyter-ai?style=flat-square&label=) | BSD-3-Clause |
| <img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="12" alt="Project Jupyter"> [JupyterLite AI](https://github.com/jupyterlite/ai) | Completion and chat, runs in the browser | ![](https://img.shields.io/github/stars/jupyterlite/ai?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/jupyterlite/ai?style=flat-square&label=) | BSD-3-Clause |
| [Notebook Intelligence](https://github.com/plmbr/notebook-intelligence) | Chat, inline edit, completion, agent mode | ![](https://img.shields.io/github/stars/plmbr/notebook-intelligence?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/plmbr/notebook-intelligence?style=flat-square&label=) | GPL-3.0 |
| [Mito AI](https://github.com/mito-ds/mito) | Context aware chat and error debugging | ![](https://img.shields.io/github/stars/mito-ds/mito?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/mito-ds/mito?style=flat-square&label=) | Mixed |
| [Jupyter AI Agents](https://github.com/datalayer/jupyter-ai-agents) | Agent that edits and runs cells | ![](https://img.shields.io/github/stars/datalayer/jupyter-ai-agents?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/datalayer/jupyter-ai-agents?style=flat-square&label=) | BSD-3-Clause |
| [genai](https://github.com/rgbkrk/genai) | Magics that read your error and your dataframes, then suggest the fix | ![](https://img.shields.io/github/stars/rgbkrk/genai?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/rgbkrk/genai?style=flat-square&label=) | BSD-3-Clause |
| [jupyter-copilot](https://github.com/baolong281/jupyter-copilot) | GitHub Copilot inline completion | ![](https://img.shields.io/github/stars/baolong281/jupyter-copilot?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/baolong281/jupyter-copilot?style=flat-square&label=) | MIT |
| 🪐 [Magic Wand](https://github.com/jupyter-ai-contrib/jupyterlab-magic-wand) | In-cell assistant with a diff view | ![](https://img.shields.io/github/stars/jupyter-ai-contrib/jupyterlab-magic-wand?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/jupyter-ai-contrib/jupyterlab-magic-wand?style=flat-square&label=) | BSD-3-Clause |

## Chat panels and agents

Generally these include a panel you type into and, can read and edit your notebook.

- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> Jupyter AI](https://github.com/jupyterlab/jupyter-ai) 🟢 - The official extension from the JupyterLab team. Version 3 connects Claude, Codex, GitHub Copilot, Gemini, Goose, Kiro, Mistral Vibe and OpenCode through the [Agent Client Protocol](https://agentclientprotocol.com). It asks permission before writing files or running commands, and several people can share one chat.
- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> JupyterLite AI](https://github.com/jupyterlite/ai) 🟢 - Completion and chat for JupyterLab, Notebook 7 and JupyterLite. It runs in the browser, so it works on a static site with no server. [Try it in the browser](https://jupyterlite.github.io/ai/lab/index.html).
- [Notebook Intelligence](https://github.com/plmbr/notebook-intelligence) 🟢 - Chat, inline edit, autocomplete and an agent that operates the notebook. Models come from GitHub Copilot, any OpenAI or LiteLLM compatible endpoint, local Ollama models, or the Claude Code CLI. GPL-3.0, so check your distribution rules before bundling it.
- [Mito AI](https://github.com/mito-ds/mito) 🟢 - Context aware chat, error debugging and an agent, installed together with the Mito spreadsheet. It is the most starred entry after Jupyter AI. The licence is mixed, so read `LICENSE` before deploying it.
- [Jupyter AI Agents](https://github.com/datalayer/jupyter-ai-agents) 🟢 - Datalayer's agent panel, built on Pydantic AI. It starts the [Jupyter MCP Server](https://github.com/datalayer/jupyter-mcp-server) as a server extension so the agent can read, write and run cells.
- [RunCell](https://pypi.org/project/runcell/) 🟢 - Agent panel from the Kanaries team, using Claude, GPT or Gemini through MCP. PyPI classifies it BSD, the shipped `LICENSE` is a copyright line with no grant, and there is no public repository ([runcell.dev](https://www.runcell.dev)).
- [Jupyter Claude Plugin](https://github.com/DCKartasoft/Jupyter-Claude_Plugin) 🟢 - Side panel built on the Claude Agent SDK that edits notebook code and markdown in place.
- [AI Terminal](https://pypi.org/project/jupyter-aiterminal/) 🟢 - Workspace of mixed AI and shell cells saved as `.agentnb` files. The AI cells are answered by the Claude Agent SDK on the server. BSD-3-Clause, no public repository.
- [LangStage](https://github.com/dkedar7/langstage-jupyter) 🟢 - Chat panel for a LangGraph DeepAgents agent, with a [walkthrough video](https://www.youtube.com/watch?v=vGA2vzMSQzo). Formerly published as `jupyter-deepagents` and `deepagent-lab`.
- [JupyDeep](https://github.com/yezhenqing/jupydeep) 🟢 - Agent engine built on Pydantic AI and MCP, for multi-step work inside one notebook.
- [Mynerva](https://github.com/NII-cloud-operation/jupyter-mynerva) 🟢 - Assistant from Japan's National Institute of Informatics that reads notebook structure and outputs before generating code, with a separate exploration mode.
- [jupyterlab-llm-assistant](https://github.com/cyneck/jupyterlab-llm-assistant) 🟢 - Small chat panel against an OpenAI compatible endpoint, with cell context.
- [jupyterlab-chat (Antony-X)](https://github.com/Antony-X/jupyterlab-chat) 🟢 - Floating chat panel that sends requests to OpenRouter. The package name is the same as the official `jupyterlab-chat`, so this one installs from source.
- [Kepler Copilot](https://pypi.org/project/keplercopilot/) 🟢 - Chat assistant panel. BSD-3-Clause, no public repository.
- [Reasonix Chat](https://github.com/orangepyt123456/jupyter-reasonix) 🟢 - Chat panel that manages remote Linux servers over SSH, including running cells in a chosen conda environment.
- [HDSP Agent](https://pypi.org/project/hdsp-jupyter-extension/) 🟢 - Thin client for a LangGraph DeepAgents server, with 161 releases on PyPI. MIT, no public repository.
- [Cellsistant](https://github.com/p4ulbr4dl3y/cellsistant) 🟡 - Chat agent that creates, runs, updates and deletes cells, and reads plots back as images.
- [pynote](https://github.com/Verflow-AI/pynote) 🟡 - Claude-powered chat side panel for JupyterLab 4 and Notebook 7.
- [Tqrar](https://github.com/marsalanjaved1/tqrar) 🟡 - Assistant panel that analyses code, explains errors and edits cells. The name is the Arabic and Urdu word for conversation. [Video](https://youtu.be/gLvrSClj-Fk).
- [ainotebookdev](https://pypi.org/project/ainotebookdev/) 🟡 - Agent tab on the right hand side. The PyPI description is a three line quick start. BSD-3-Clause, no public repository.
- [mcp-client-jupyter-chat](https://github.com/ihrpr/mcp-client-jupyter-chat) ⚪ - Early MCP client in a chat panel, from one of the MCP authors.
- [jupyterlab-notechat](https://github.com/firezym/jupyterlab-notechat) ⚪ - Chat that treats the notebook itself as the conversation, with reference marks between cells.
- [jupyter-ollama-ai](https://github.com/bhumukul-raj/jupyter-ollama-ai) ⚪ - Ollama chat and cell actions, entirely local.
- [jupyterchatz](https://github.com/Zhoums396/jupyterchatz) ⚪ - Chat panel with MCP support.
- [Pieces for JupyterLab](https://pypi.org/project/jupyter-pieces/) ⚪ - Snippet capture and workstream context, shared with the vendor's editor plugins. MIT, and the repository it points at is not public ([docs.pieces.app](https://docs.pieces.app/)).
- [Jovyan AI](https://pypi.org/project/jovyanai-extension/) ⚪ - Completion and chat. BSD-3-Clause, no public repository.
- [Sage Agent](https://pypi.org/project/sage-agent-internal/) ⚪ - Notebook assistant. BSD-3-Clause, no public repository ([sagebook.ai](https://sagebook.ai/)).
- [escobar](https://pypi.org/project/escobar/) ⚪ - Chat extension with 142 releases and a placeholder repository URL that has never been filled in. BSD-3-Clause.

<table>
<tr>
<td width="33%"><a href="https://github.com/jupyterlab/jupyter-ai"><img src="https://raw.githubusercontent.com/jupyterlab/jupyter-ai/main/docs/source/_static/chat-explain-code-output.png" alt="Jupyternaut explaining the cell you dropped into the chat"></a><br><sub><b>Jupyter AI</b>: Jupyternaut explaining the cell you dropped into the chat</sub></td>
<td width="33%"><a href="https://github.com/plmbr/notebook-intelligence"><img src="https://raw.githubusercontent.com/plmbr/notebook-intelligence/main/media/copilot-chat.gif" alt="asking about the open notebook"></a><br><sub><b>Notebook Intelligence</b>: asking about the open notebook</sub></td>
<td width="33%"><a href="https://github.com/datalayer/jupyter-ai-agents"><img src="https://images.datalayer.io/product/jupyter-ai-agents/jupyterlab-example-1.png" alt="the agent creates the notebook, installs matplotlib and runs it"></a><br><sub><b>Jupyter AI Agents</b>: the agent creates the notebook, installs matplotlib and runs it</sub></td>
</tr>
</table>

## Inline completion

Ghost text as you type, through the JupyterLab completer API.

- [jupyter-copilot](https://github.com/baolong281/jupyter-copilot) ⚪ - Runs the `copilot.vim` language server as the backend of the JupyterLab completer. It is the simplest way to get GitHub Copilot in a notebook. Authentication on the extension server is disabled, so do not use it over SSH.
- [jupyterlab-browser-ai](https://github.com/jtpio/jupyterlab-browser-ai) 🟡 - Uses Chrome's built-in AI APIs, so it needs no API key and sends no data off the machine. Needs Chrome flags turned on. [Try it in the browser](https://jtpio.github.io/jupyterlab-browser-ai/lab/index.html).
- [llm-complete](https://github.com/pb1729/llm-complete) 🟡 - Minimal inline completion provider, useful as a template.
- [Pocket Coder](https://github.com/Param302/Pocket-Coder) 🟡 - A 1.2B model on Ollama giving offline completion in notebooks and VS Code. Fine-tuned from LiquidAI LFM 2.5.
- [jupyter-copilot-completer](https://github.com/StFroese/jupyter-copilot-completer) ⚪ - Also runs the Copilot language server through the completer API.
- [codeium.jupyter](https://github.com/Exafunction/codeium.jupyter) ⚪ - Codeium's own JupyterLab client. It has not been updated since Codeium became Windsurf.

<table>
<tr>
<td width="60%"><a href="https://github.com/baolong281/jupyter-copilot"><img src="https://github.com/baolong281/jupyter-copilot/blob/656c425c9956eb1563a3f90990e0b270ebff725f/imgs/demo.gif?raw=true" alt="GitHub Copilot suggesting the next line"></a><br><sub><b>jupyter-copilot</b>: GitHub Copilot suggesting the next line</sub></td>
</tr>
</table>

## In-cell edits and magics

Help inside the cell you are editing: a button on the cell toolbar, a magic, or a diff you accept.

- [🪐 Magic Wand](https://github.com/jupyter-ai-contrib/jupyterlab-magic-wand) ⚪ - In-cell assistant: describe what you want in the cell and accept or reject the diff. Its diff view and cell footer were split out into [jupyterlab-diff](https://github.com/jupyter-ai-contrib/jupyterlab-diff) and [jupyterlab-cell-input-footer](https://github.com/jupyter-ai-contrib/jupyterlab-cell-input-footer). [Try it on Binder](https://mybinder.org/v2/gh/jupyter-ai-contrib/jupyterlab-magic-wand/main?urlpath=lab).
- [ai-jup](https://github.com/AnswerDotAI/ai-jup) 🟡 - Prompt cells with ``$`variable` `` to inject kernel values and ``&`function` `` to expose Python functions as tools, inspired by fast.ai's Solveit. The author states it is an experiment and not maintained long term. GPL-3.0.
- [jupyter-vibe-coding](https://github.com/haesleinhuepf/jupyter-vibe-coding) 🟡 - Explain, Fix and Generate buttons on the cell toolbar. Explain and Fix trigger on a traceback. The code is short, so read it first if you are writing your own.
- [jupyterlite-ai-kernels](https://github.com/jtpio/jupyterlite-ai-kernels) 🟡 - Registers one kernel per configured provider, so a cell is a prompt and the reply streams back as output. [Try it in the browser](https://jtpio.github.io/jupyterlite-ai-kernels/lab/index.html).
- [jupyter-ext-ai](https://github.com/novatechnolab/jupyter-ext-ai) 🟡 - Magic commands for chatting with OpenAI, Gemini and Claude from a cell.
- [CoML](https://github.com/microsoft/CoML) ⚪ - Microsoft Research assistant with three modes, including one that suggests what to try next on a machine learning task. The readme has demo GIFs.

<table>
<tr>
<td width="50%"><a href="https://github.com/jupyter-ai-contrib/jupyterlab-magic-wand"><img src="https://raw.githubusercontent.com/jupyter-ai-contrib/jupyterlab-magic-wand/main/docs/README.png" alt="describe the cell you want, accept the diff"></a><br><sub><b>Magic Wand</b>: describe the cell you want, accept the diff</sub></td>
<td width="50%"><a href="https://github.com/microsoft/CoML"><img src="https://raw.githubusercontent.com/microsoft/CoML/main/assets/demo_coml.gif" alt="a magic that fills in the next step"></a><br><sub><b>CoML</b>: a magic that fills in the next step</sub></td>
</tr>
</table>

## Agent CLI bridges

Claude Code, Codex and the other CLI agents run in a terminal. These extensions connect the notebook to that agent, through a side panel, a magic or cell comments.

- [AI Code Assistants](https://github.com/stellarshenson/jupyterlab_ai_code_assistants_extension) 🟢 - Start, resume, fork and clean up CLI sessions for Claude Code, Codex, Kimi, Gemini and DeepSeek from one side panel per assistant. It replaces the author's separate `jupyterlab_claude_code_extension` and `jupyterlab_codex_extension` packages and migrates their settings.
- [jupyterlab-codex](https://github.com/oy-ilho/jupyterlab-codex) 🟢 - Codex CLI in a sidebar, with a server extension to keep the session alive.
- [Yukti](https://github.com/sizhky/jupyterlab-yukti) 🟢 - A `%%ask` magic that sends everything visible above the current cell, markdown and outputs included, to the Codex CLI.
- [xtralab](https://github.com/jtpio/xtralab) 🟢 - Meta-package that reshapes JupyterLab around CLI agents, with an agent launcher and an MCP server for interacting with the JupyterLab interface and performing actions on files and notebooks. It comes with a set of extensions and opinionated defaults, and also offers a desktop app for macOS and Linux.
- [jupyter-codex](https://github.com/yanndebray/jupyterlab-codex) 🟡 - Opens an OpenAI Codex chat in the left sidebar.
- [nb-margin](https://pypi.org/project/nb-margin/) 🟡 - Annotate cells with comments, then send them all to Claude Code. Claude Code edits the `.ipynb` file and the notebook reloads. MIT, copyright Anthropic, and the repository it points at is not public.

<table>
<tr>
<td width="50%"><a href="https://github.com/stellarshenson/jupyterlab_ai_code_assistants_extension"><img src="https://raw.githubusercontent.com/stellarshenson/jupyterlab_ai_code_assistants_extension/main/.resources/screenshot.png" alt="one side panel per assistant"></a><br><sub><b>AI Code Assistants</b>: one side panel per assistant</sub></td>
<td width="50%"><a href="https://github.com/oy-ilho/jupyterlab-codex"><img src="https://raw.githubusercontent.com/oy-ilho/jupyterlab-codex/main/docs/images/codex-sidebar-screenshot.png" alt="the Codex CLI in a sidebar"></a><br><sub><b>jupyterlab-codex</b>: the Codex CLI in a sidebar</sub></td>
</tr>
</table>

## Domain, teaching and platform

Built for one scientific field, one classroom or one vendor platform.

- [Jupyter AI Tutor](https://github.com/QuantStack/jupyter-ai-tutor) 🟢 - Adds an Explain Code button to every code cell. The button opens a chat with the cell, its output and the surrounding notebook as context. Built for teaching. [Try it on Binder](https://mybinder.org/v2/gh/QuantStack/jupyter-ai-tutor/main?urlpath=lab).
- [jupytutor](https://github.com/team-jupytutor/jupytutor) 🟢 - Gives students LLM feedback based on their autograder results plus course context supplied by the instructor.
- [FlowBook](https://github.com/stephenfreund/FlowBook) 🟢 - Marks cells whose inputs have changed, so re-running any cell gives the same answer as a top to bottom run. For each violation it reports, it can ask an LLM to diagnose the cause and offer one-click fixes. Without an API key the LLM part is off and the rest still works.
- [CRANE-LLM](https://github.com/PELAB-LiU/crane_llm) 🟢 - Research extension that predicts and diagnoses notebook crashes at runtime, against OpenAI, Gemini or Ollama.
- [jupyter-geoagent](https://github.com/geojupyter/jupyter-geoagent) 🟢 - Map explorer for STAC catalogs with an MCP query interface over DuckDB, and reproducible exports of what the agent did.
- [GeoCopilot](https://pypi.org/project/opengeolab-geocopilot/) 🟢 - Codex-powered notebook agent for geospatial work, on top of `jupyter-server-mcp`. MIT, no public repository.
- [InstrMCP](https://github.com/caidish/instrMCP) 🟢 - MCP server suite that lets a model read QCodes instruments and measurement databases from a JupyterLab session in a physics lab.
- [smarts.bio](https://github.com/smartsbio/smarts-bio-jupyterlab) 🟢 - Bioinformatics agent that runs GPU pipelines such as RFdiffusion and Boltz, searches NCBI, UniProt and PDB, and opens FASTA, BAM, VCF and PDB files natively. Commercial, with an MIT wrapper package ([smarts.bio](https://smarts.bio)).
- [Lightcone Lab](https://pypi.org/project/jupyterlab-lightcone/) 🟢 - Research workbench that connects analyses, cited papers and materialised outputs, with optional Jupyter AI integration. BSD-3-Clause, no public repository.
- [SageMaker GenAI extension](https://pypi.org/project/sagemaker-gen-ai-jupyterlab-extension/) 🟢 - Amazon's GenAI and Q Developer extensions, published for the JupyterLab images inside SageMaker Studio.
- [Xavier](https://github.com/CHI25-Xavier/Xavier) 🟡 - Research prototype from a CHI'25 paper on tabular data wrangling. It keeps the data in view while it suggests code. [Paper](https://doi.org/10.1145/3706598.3714239), [video](https://youtu.be/KTnCHSv1heI).
- [Auto Dashboards](https://github.com/orbrx/auto-dashboards) 🟡 - Turns a notebook into a Streamlit, Dash or Solara dashboard and previews it beside the notebook.
- [WWC Copilot](https://github.com/adamisom/jupyterlab-research-assistant-wwc-copilot) 🟡 - Academic research library with Semantic Scholar and OpenAlex import, PDF parsing and AI metadata extraction.
- [LLM Attributor](https://github.com/poloclub/LLM-Attributor) ⚪ - Georgia Tech widget that attributes generated text back to training data.
- [hintbot](https://github.com/educational-technology-collective/hintbot) ⚪ - Asks for a hint on the current cell in a teaching setting, and logs the request.

<table>
<tr>
<td width="33%"><a href="https://github.com/smartsbio/smarts-bio-jupyterlab"><img src="https://smarts-public.s3.us-east-1.amazonaws.com/jupyterlab/screenshot-structure-chat.png" alt="a protein structure answered in the chat"></a><br><sub><b>smarts.bio</b>: a protein structure answered in the chat</sub></td>
<td width="33%"><a href="https://github.com/poloclub/LLM-Attributor"><img src="https://raw.githubusercontent.com/poloclub/LLM-Attributor/master/assets/crownjewel.png" alt="an answer traced back to the training data behind it"></a><br><sub><b>LLM Attributor</b>: an answer traced back to the training data behind it</sub></td>
<td width="33%"><a href="https://github.com/CHI25-Xavier/Xavier"><img src="https://raw.githubusercontent.com/CHI25-Xavier/Xavier/master/assets/UI_Overview.png" alt="data kept in view while code is suggested"></a><br><sub><b>Xavier</b>: data kept in view while code is suggested</sub></td>
</tr>
</table>

## Building blocks

Plugins and libraries to build on. Few of them do anything on their own, and Jupyter AI v3 is assembled from them: installing `jupyter-ai` installs nine of the packages below, and its extras install six more. Every code repository in [jupyter-ai-contrib](https://github.com/jupyter-ai-contrib) is listed somewhere in this file, most of them here.

### Jupyter AI plugins

- [🪐 jupyter-ai-persona-manager](https://github.com/jupyter-ai-contrib/jupyter-ai-persona-manager) 🟢 - Registry that turns a class into a named participant in a chat.
- [🪐 jupyter-ai-jupyternaut](https://github.com/jupyter-ai-contrib/jupyter-ai-jupyternaut) 🟢 - Jupyternaut, the default persona, and the reference for writing another.
- [🪐 jupyter-ai-router](https://github.com/jupyter-ai-contrib/jupyter-ai-router) 🟢 - Routes each chat message to a persona.
- [🪐 jupyter-ai-litellm](https://github.com/jupyter-ai-contrib/jupyter-ai-litellm) 🟢 - Model abstraction over LiteLLM. This is how v3 connects to a model provider.
- [🪐 jupyter-ai-acp-client](https://github.com/jupyter-ai-contrib/jupyter-ai-acp-client) 🟢 - Agent Client Protocol client, the piece that lets external agents appear in the chat.
- [🪐 jupyter-ai-claude-code](https://github.com/jupyter-ai-contrib/jupyter-ai-claude-code) 🟡 - Jupyter AI persona that runs Claude Code.
- [🪐 jupyter-ai-personas](https://github.com/jupyter-ai-contrib/jupyter-ai-personas) ⚪ - Example personas for Jupyter AI v2, kept for reference.
- [🪐 jupyter-ai-chat-commands](https://github.com/jupyter-ai-contrib/jupyter-ai-chat-commands) 🟡 - Slash commands in the chat input.
- [🪐 jupyter-ai-tools](https://github.com/jupyter-ai-contrib/jupyter-ai-tools) 🟢 - Tool implementations for agents working on notebooks and files.
- [🪐 jupyter-ai-magic-commands](https://github.com/jupyter-ai-contrib/jupyter-ai-magic-commands) 🟢 - The v3 replacement for `jupyter-ai-magics`, built on LiteLLM.
- [🪐 jupyter-ai-demos](https://github.com/jupyter-ai-contrib/jupyter-ai-demos) 🟡 - Notebooks and custom personas demonstrating what Jupyter AI v3 can do. Read the personas before writing your own.

### Chat and notebook UI

- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> Jupyter Chat](https://github.com/jupyterlab/jupyter-chat) 🟢 - The chat document, the React components and the `jupyterlab-chat` extension. Install it alone for a chat between humans, or depend on it to write your own assistant. [Try it on Binder](https://mybinder.org/v2/gh/jupyterlab/jupyter-chat/main?urlpath=lab).
- [🪐 jupyter-chat-components](https://github.com/jupyter-ai-contrib/jupyter-chat-components) 🟢 - Extra components to display inside a chat. [Try it in the browser](https://jupyter-ai-contrib.github.io/jupyter-chat-components/lab/index.html?path=components_demo.ipynb).
- [🪐 jupyter-floating-chat](https://github.com/jupyter-ai-contrib/jupyter-floating-chat) 🟡 - Chat input that floats over the document.
- [🪐 jupyterlab-diff](https://github.com/jupyter-ai-contrib/jupyterlab-diff) 🟢 - Cell and file diffs with several strategies, for showing what an agent proposes. [Try it in the browser](https://jupyter-ai-contrib.github.io/jupyterlab-diff/lab/index.html?path=diff-demo.ipynb).
- [🪐 jupyterlab-cell-input-footer](https://github.com/jupyter-ai-contrib/jupyterlab-cell-input-footer) 🟡 - A place under a cell input to put your own UI.
- [🪐 jupyterlab-ai-commands](https://github.com/jupyter-ai-contrib/jupyterlab-ai-commands) 🟢 - JupyterLab commands written for agents to call.
- [🪐 jupyterlab-commands-toolkit](https://github.com/jupyter-ai-contrib/jupyterlab-commands-toolkit) 🟢 - Exposes the JupyterLab command registry as an AI toolkit.
- [🪐 jupyterlab-notebook-awareness](https://github.com/jupyter-ai-contrib/jupyterlab-notebook-awareness) 🟡 - Publishes the current notebook and the active cell into the awareness state, so an agent can read where the cursor is.
- [🪐 jupyterlab-document-collaborators](https://github.com/jupyter-ai-contrib/jupyterlab-document-collaborators) 🟡 - Shows who else has the document open, along the top of it.
- [jupyterlab_voice_capture_extension](https://github.com/stellarshenson/jupyterlab_voice_capture_extension) 🟢 - Streams the browser microphone to a server side FIFO, so a CLI agent in a container can use voice mode.

<table>
<tr>
<td width="60%"><a href="https://github.com/jupyterlab/jupyter-chat"><img src="https://raw.githubusercontent.com/jupyterlab/jupyter-chat/main/python/jupyterlab-chat/screenshot.gif" alt="the shared chat document Jupyter AI is built on"></a><br><sub><b>Jupyter Chat</b>: the shared chat document Jupyter AI is built on</sub></td>
</tr>
</table>

### Live reload

An agent writes to the notebook file while you have it open. By default JupyterLab keeps showing the old cells as reloading the document could lose the widget state. These extensions instead update the open notebook when the file changes.

- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> jupyter-collaboration](https://github.com/jupyterlab/jupyter-collaboration) 🟢 - Real time collaboration on Yjs. It is what lets two people, or a person and an agent, type into one notebook. Jupyter AI installs it under the `rtc` extra.
- [🪐 jupyter-live-content](https://github.com/jupyter-ai-contrib/jupyter-live-content) 🟢 - Live file content updates, so the UI follows an agent editing on disk.
- [🪐 jupyter-server-documents](https://github.com/jupyter-ai-contrib/jupyter-server-documents) 🟢 - Keeps document and kernel state on the server with pycrdt, for faster updates and lower memory. Jupyter AI installs it under the `rtc-jsd` extra.
- [hot-notebook-patching](https://github.com/kolibril13/hot-notebook-patching) 🟢 - Patches only the cells that changed, so the kernel keeps running and widgets keep their state. Written for notebooks edited by Claude Code.
- [jupyterlab-claude-code-refresh](https://github.com/wenatuhs/jupyterlab-claude-code-refresh) ⚪ - Reloads the open notebook from disk when Claude Code edits the file.

### MCP

An MCP server lets an agent that runs outside JupyterLab read and edit a notebook. It also lets an extension offer its own commands as tools.

- [Jupyter MCP Server](https://github.com/datalayer/jupyter-mcp-server) 🟢 - The most starred MCP server for Jupyter. Lets any MCP client read, write and run cells, including multimodal output.
- [cursor-notebook-mcp](https://github.com/jbeno/cursor-notebook-mcp) 🟡 - MCP server that edits `.ipynb` files for an agent that has no notebook UI of its own, written for Cursor.
- [🪐 jupyter-server-mcp](https://github.com/jupyter-ai-contrib/jupyter-server-mcp) 🟢 - Jupyter Server extension that registers Python functions as MCP tools from inside the server. Jupyter AI uses it.
- [jupyter-mcp-tools](https://github.com/datalayer/jupyter-mcp-tools) 🟢 - Exposes JupyterLab commands as MCP tools.
- [🪐 jupyter-mcp-manager](https://github.com/jupyter-ai-contrib/jupyter-mcp-manager) 🟢 - UI and backend for configuring which MCP servers are available to other extensions.
- [🪐 jupyter-server-ai-tools](https://github.com/jupyter-ai-contrib/jupyter-server-ai-tools) ⚪ - Jupyter Server extension that collects the tools other extensions declare, so an agent can list them from one place.
- [MCP Console](https://pypi.org/project/jupyterlab-mcp-console/) 🟢 - Discover, inspect and deploy MCP servers through an AgentRegistry API. BSD-3-Clause, no public repository.

<table>
<tr>
<td width="50%"><a href="https://github.com/datalayer/jupyter-mcp-tools"><img src="https://images.datalayer.io/products/jupyter-mcp-tools/jupyter-mcp-tools.gif" alt="JupyterLab commands called as MCP tools"></a><br><sub><b>jupyter-mcp-tools</b>: JupyterLab commands called as MCP tools</sub></td>
<td width="50%"><a href="https://github.com/jupyter-ai-contrib/jupyter-mcp-manager"><img src="https://raw.githubusercontent.com/jupyter-ai-contrib/jupyter-mcp-manager/main/MCP-manager-settings-panel.png" alt="choosing which MCP servers are available"></a><br><sub><b>jupyter-mcp-manager</b>: choosing which MCP servers are available</sub></td>
</tr>
</table>

## Beyond the JupyterLab UI

These are not JupyterLab extensions. They are command line tools, magics and models that a notebook user runs next to Jupyter.

- [🪐 nb-cli](https://github.com/jupyter-ai-contrib/nb-cli) 🟢 - Command line for notebooks with an AI-optimised markdown format, so an agent can work without a browser.
- [jupyterlab-cli](https://github.com/wenmin-wu/jupyterlab-cli) 🟡 - CLI where every command is one HTTP call to the server, plus clipboard and context helpers in the UI.
- [genai](https://github.com/rgbkrk/genai) 🟡 - IPython magics that read your error and your dataframes before suggesting a fix. Written at Noteable, a notebook company that later shut down.
- [agent-client-kernel](https://github.com/jimwhite/agent-client-kernel) 🟡 - A kernel that connects to an agent over the Agent Client Protocol, so the agent answers your cells wherever a kernel can run.
- [chatlab](https://github.com/rgbkrk/chatlab) ⚪ - Library for trying out tool calling in a notebook, with the model able to call functions you defined in the cell above.
- [codebind](https://github.com/ghovax/codebind) 🟢 - Agent that runs the conversation and leaves execution, namespace and display to IPython.
- [jupyter-agents-kit](https://github.com/p4ulbr4dl3y/jupyter-agents-kit) 🟡 - Small fine-tuned models for JupyterLab cell manipulation, with datasets published.
- [Elyra](https://github.com/elyra-ai/elyra) 🟢 - Runs notebooks as pipelines on Kubeflow Pipelines and Apache Airflow, and predates the LLM extensions. It is still the largest set of JupyterLab extensions for machine learning work.
- [ajlab](https://github.com/jtpio/ajlab) 🟢 - Meta-package that installs JupyterLab plus the extensions and settings an agent workflow needs.

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) first. It has the listing criteria, including what is deliberately left out, how an entry gets its marker, and how the list was assembled.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
