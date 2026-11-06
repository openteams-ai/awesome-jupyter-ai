# Awesome Jupyter AI [![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

> AI extensions for JupyterLab and Jupyter Notebook 7 | [Blog post](https://openteams.com/engineering-blog/awesome-jupyter-ai-extensions/)

We are excited to see the Jupyter extension ecosystem thrive in the era of AI. The variety of ideas and implementations demonstrates the utility of the extension platform and the API stability offered by JupyterLab. This list collects over a hundred AI extensions for JupyterLab and Jupyter Notebook 7. They range from chat panels and inline completers to teaching tools and the building blocks of Jupyter AI. Each one installs into a JupyterLab or Notebook 7 you already run.

The authors include individuals, universities, research institutes and corporations. Listing an extension here is not an endorsement.

## Contents

- [How this list is organised](#how-this-list-is-organised)
- [At a glance](#at-a-glance)
- [Chat panels and agents](#chat-panels-and-agents)
- [Inline completion](#inline-completion)
- [In-cell edits](#in-cell-edits)
- [Agent CLI bridges](#agent-cli-bridges)
- [Domain, teaching and platform](#domain-teaching-and-platform)
- [Building blocks](#building-blocks)
  - [Jupyter AI plugins](#jupyter-ai-plugins)
  - [Chat and notebook UI](#chat-and-notebook-ui)
  - [Live reload](#live-reload)
  - [MCP](#mcp)
- [IPython](#ipython)
- [Beyond the JupyterLab UI](#beyond-the-jupyterlab-ui)
- [Agent skills](#agent-skills)

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
| <img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="12" alt="Project Jupyter"> [Jupyter AI Lite](https://github.com/jupyterlab/jupyter-ai-lite) | Completion and chat, runs in the browser | ![](https://img.shields.io/github/stars/jupyterlab/jupyter-ai-lite?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/jupyterlab/jupyter-ai-lite?style=flat-square&label=) | BSD-3-Clause |
| [Notebook Intelligence](https://github.com/plmbr/notebook-intelligence) | Chat, inline edit, completion, agent mode | ![](https://img.shields.io/github/stars/plmbr/notebook-intelligence?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/plmbr/notebook-intelligence?style=flat-square&label=) | GPL-3.0 |
| [Mito AI](https://github.com/mito-ds/mito) | Context aware chat and error debugging | ![](https://img.shields.io/github/stars/mito-ds/mito?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/mito-ds/mito?style=flat-square&label=) | Mixed |
| [Jupyter AI Agents](https://github.com/datalayer/jupyter-ai-agents) | Agent that edits and runs cells | ![](https://img.shields.io/github/stars/datalayer/jupyter-ai-agents?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/datalayer/jupyter-ai-agents?style=flat-square&label=) | BSD-3-Clause |
| [genai](https://github.com/rgbkrk/genai) | Magics that read your error and your dataframes, then suggest the fix | ![](https://img.shields.io/github/stars/rgbkrk/genai?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/rgbkrk/genai?style=flat-square&label=) | BSD-3-Clause |
| [jupyter-copilot](https://github.com/baolong281/jupyter-copilot) | GitHub Copilot inline completion | ![](https://img.shields.io/github/stars/baolong281/jupyter-copilot?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/baolong281/jupyter-copilot?style=flat-square&label=) | MIT |
| 🪐 [Magic Wand](https://github.com/jupyter-ai-contrib/jupyterlab-magic-wand) | In-cell assistant with a diff view | ![](https://img.shields.io/github/stars/jupyter-ai-contrib/jupyterlab-magic-wand?style=flat-square&label=) | ![](https://img.shields.io/github/last-commit/jupyter-ai-contrib/jupyterlab-magic-wand?style=flat-square&label=) | BSD-3-Clause |

## Chat panels and agents

Generally these include a panel you type into and, can read and edit your notebook.

- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> Jupyter AI](https://github.com/jupyterlab/jupyter-ai) 🟢 - The official extension from the JupyterLab team. Version 3 connects Claude, Codex, GitHub Copilot, Goose, Kilo, Kiro, Mistral Vibe and OpenCode through the [Agent Client Protocol](https://agentclientprotocol.com). It asks permission before writing files or running commands, and several people can share one chat.
- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> Jupyter AI Lite](https://github.com/jupyterlab/jupyter-ai-lite) 🟢 - Jupyter AI's Jupyternaut persona running in the browser, with chat and completion in JupyterLab, Notebook 7 and JupyterLite, so it works on a static site with no server. Version 0.21.0 renamed the `jupyterlite-ai` package to `jupyter-ai-lite` and split out `jupyter-ai-agent-lite`, the building blocks for writing another in-browser persona. [Try it in the browser](https://jupyterlab.github.io/jupyter-ai-lite/lab/index.html).
- [Notebook Intelligence](https://github.com/plmbr/notebook-intelligence) 🟢 - Chat, inline edit, autocomplete, an agent that operates the notebook, and Chatbook, a kernel where a cell can be an English prompt that generates code and runs it in a kernel you choose. Models come from GitHub Copilot, any OpenAI or LiteLLM compatible endpoint, local Ollama models, or the Claude Code CLI. GPL-3.0, so check your distribution rules before bundling it.
- [Mito AI](https://github.com/mito-ds/mito) 🟡 - Context aware chat, error debugging and an agent, installed together with the Mito spreadsheet. It is the most starred entry after Jupyter AI. The licence is mixed, so read `LICENSE` before deploying it.
- [Jupyter AI Agents](https://github.com/datalayer/jupyter-ai-agents) 🟢 - Datalayer's agent panel, built on Pydantic AI. It starts the [Jupyter MCP Server](https://github.com/datalayer/jupyter-mcp-server) as a server extension so the agent can read, write and run cells.
- [RunCell](https://pypi.org/project/runcell/) 🟢 - Agent panel from the Kanaries team, using Claude, GPT or Gemini through MCP. PyPI classifies it BSD, the shipped `LICENSE` is a copyright line with no grant, and there is no public repository ([runcell.dev](https://www.runcell.dev)).
- [Jupyter Claude Plugin](https://github.com/DCKartasoft/Jupyter-Claude_Plugin) 🟢 - Side panel built on the Claude Agent SDK that edits notebook code and markdown in place.
- [AI Terminal](https://pypi.org/project/jupyter-aiterminal/) 🟢 - Workspace of mixed AI and shell cells saved as `.agentnb` files. The AI cells are answered by the Claude Agent SDK on the server. BSD-3-Clause, no public repository.
- [LangStage](https://github.com/dkedar7/langstage-jupyter) 🟢 - Chat panel for a LangGraph DeepAgents agent, with a [walkthrough video](https://www.youtube.com/watch?v=vGA2vzMSQzo). Formerly published as `jupyter-deepagents` and `deepagent-lab`.
- [JupyDeep](https://github.com/yezhenqing/jupydeep) 🟢 - Agent engine built on Pydantic AI and MCP, for multi-step work inside one notebook.
- [jupyterlab-llm-assistant](https://github.com/cyneck/jupyterlab-llm-assistant) 🟢 - Small chat panel against an OpenAI compatible endpoint, with cell context.
- [jupyterlab-chat (Antony-X)](https://github.com/Antony-X/jupyterlab-chat) 🟢 - Floating chat panel that sends requests to OpenRouter. The package name is the same as the official `jupyterlab-chat`, so this one installs from source.
- [Reasonix Chat](https://github.com/orangepyt123456/jupyter-reasonix) 🟢 - Chat panel that manages remote Linux servers over SSH, including running cells in a chosen conda environment.
- [Codebuff Agent](https://pypi.org/project/codebuff-agent/) 🟢 - Thin client for a LangGraph DeepAgents server, published as `hdsp-jupyter-extension` until version 2.1.73. MIT, no public repository.
- [Whybook](https://github.com/openteams-ai/whybook) 🟢 - Research prototype of a notebook view with no chat box: drag a column onto a cell, pick one of the questions it offers, and a template or an agent adds and runs the cells that answer it. Each cell shows the constants and defaults its result depends on, as chips you can question. [Try it on Binder](https://mybinder.org/v2/gh/openteams-ai/whybook/main?urlpath=lab/tree/examples/pain_diary/pain_diary_cohort.ipynb).
- [Mynerva](https://github.com/NII-cloud-operation/jupyter-mynerva) 🟢 - Assistant from Japan's National Institute of Informatics that reads notebook structure and outputs before generating code, with a separate exploration mode.
- [verknode](https://github.com/verknode-project/verknode) 🟢 - Node-based workflow editor on a JupyterLab canvas, where about 300 nodes pass polars tables to each other, LLM nodes prompt a model for every row, and an agent in a chat on the canvas adds and connects nodes. It installs from the wheel attached to a GitHub release or as a Docker image, because the `verknode` package on PyPI is a placeholder. [Try it in the browser](https://verknode-project.github.io/verknode/lab/index.html?path=examples/demo.vkf).
- [Kepler Copilot](https://pypi.org/project/keplercopilot/) 🟡 - Chat assistant panel. BSD-3-Clause, no public repository.
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

<table>
<tr>
<td width="60%"><a href="https://github.com/baolong281/jupyter-copilot"><img src="https://github.com/baolong281/jupyter-copilot/blob/656c425c9956eb1563a3f90990e0b270ebff725f/imgs/demo.gif?raw=true" alt="GitHub Copilot suggesting the next line"></a><br><sub><b>jupyter-copilot</b>: GitHub Copilot suggesting the next line</sub></td>
</tr>
</table>

## In-cell edits

Help inside the cell you are editing: a button on the cell toolbar, a prompt cell, or a diff you accept.

- [🪐 Magic Wand](https://github.com/jupyter-ai-contrib/jupyterlab-magic-wand) ⚪ - In-cell assistant: describe what you want in the cell and accept or reject the diff. Its diff view and cell footer were split out into [jupyterlab-diff](https://github.com/jupyter-ai-contrib/jupyterlab-diff) and [jupyterlab-cell-input-footer](https://github.com/jupyter-ai-contrib/jupyterlab-cell-input-footer). [Try it on Binder](https://mybinder.org/v2/gh/jupyter-ai-contrib/jupyterlab-magic-wand/main?urlpath=lab).
- [ai-jup](https://github.com/AnswerDotAI/ai-jup) 🟡 - Prompt cells with ``$`variable` `` to inject kernel values and ``&`function` `` to expose Python functions as tools, inspired by fast.ai's Solveit. The author states it is an experiment and not maintained long term. GPL-3.0.
- [nbinlineai](https://github.com/rahuldave/nbinlineai) 🟢 - Prompt cells in the style of ai-jup, with ``$`variable` `` for a live kernel value and ``&`function` `` to let the model call your Python function, and each answer saved as an editable Markdown cell. It works with an OpenAI or Anthropic API key or a ChatGPT sign-in, and is GPL-3.0.
- [Plottery](https://github.com/brianhempel/plottery) 🟢 - Replaces the image from `plt.show()` with an editor where you drag shapes, change arguments with a live preview, or ask a model to change the plot, and each change is written back into the cell's code. It is a research prototype from a VL/HCC 2026 paper, installed as `plottery-ui` because `plottery` on PyPI is a different package. [Paper](https://plottery.org/assets/Plottery-%20A%20Code-Integrated%20GUI%20for%20Matplotlib%20Preprint%20with%20Appendix.pdf), [video](https://plottery.org/assets/Plottery%20Video%20Figure.mp4).
- [jupyter-vibe-coding](https://github.com/haesleinhuepf/jupyter-vibe-coding) 🟡 - Explain, Fix and Generate buttons on the cell toolbar. Explain and Fix trigger on a traceback. The code is short, so read it first if you are writing your own.
- [jupyterlite-ai-kernels](https://github.com/jtpio/jupyterlite-ai-kernels) 🟡 - Registers one kernel per configured provider, so a cell is a prompt and the reply streams back as output. [Try it in the browser](https://jtpio.github.io/jupyterlite-ai-kernels/lab/index.html).

<table>
<tr>
<td width="50%"><a href="https://github.com/jupyter-ai-contrib/jupyterlab-magic-wand"><img src="https://raw.githubusercontent.com/jupyter-ai-contrib/jupyterlab-magic-wand/main/docs/README.png" alt="describe the cell you want, accept the diff"></a><br><sub><b>Magic Wand</b>: describe the cell you want, accept the diff</sub></td>
<td width="50%"><a href="https://github.com/haesleinhuepf/jupyter-vibe-coding"><img src="https://raw.githubusercontent.com/haesleinhuepf/jupyter-vibe-coding/main/docs/images/teaser.gif" alt="Explain and Fix buttons under a traceback"></a><br><sub><b>jupyter-vibe-coding</b>: Explain and Fix buttons under a traceback</sub></td>
</tr>
</table>

## Agent CLI bridges

Claude Code, Codex and the other CLI agents run in a terminal. These extensions connect the notebook to that agent, through a side panel, a magic or cell comments.

- [AI Code Assistants](https://github.com/stellarshenson/jupyterlab_ai_code_assistants_extension) 🟢 - Start, resume, fork and clean up CLI sessions for Claude Code, Codex, Kimi, Gemini and DeepSeek from one side panel per assistant. It replaces the author's separate `jupyterlab_claude_code_extension`, `jupyterlab_codex_extension` and `jupyterlab_kimi_code_extension` packages and migrates their settings.
- [Yukti](https://github.com/sizhky/jupyterlab-yukti) 🟢 - A `%%ask` magic that sends everything visible above the current cell, markdown and outputs included, to the Codex CLI.
- [xtralab](https://github.com/jtpio/xtralab) 🟢 - Meta-package that reshapes JupyterLab around CLI agents, with an agent launcher and an MCP server for interacting with the JupyterLab interface and performing actions on files and notebooks. It comes with a set of extensions and opinionated defaults, and also offers a desktop app for macOS and Linux.
- [ajlab](https://github.com/jtpio/ajlab) 🟢 - Meta-package that installs JupyterLab with `jupyter-server-mcp`, `jupyterlab-commands-toolkit` and the collaboration document server. A CLI agent in a JupyterLab terminal can then run JupyterLab commands in your browser tab, and an open notebook updates when the agent edits the file.
- [jupyter-pair](https://github.com/fakhirali/jupyter-pair) 🟢 - OpenCode plugin and agent skill that join the open notebook as a collaboration client, so cells the agent adds, edits and runs appear live in your JupyterLab tab. The agent cannot change or run a cell you edited since it last read it, and it needs OpenCode 2 and `jupyter-collaboration`.
- [🪐 jupyter-ai-pi-lite](https://github.com/jupyter-ai-contrib/jupyter-ai-pi-lite) 🟢 - Experimental package that runs the [pi coding agent](https://pi.dev) in the browser, as a Jupyter AI persona in the chat and as the `pi` command in the JupyterLite terminal. The two share tools, settings, credentials and sessions, and are built on `jupyter-ai-agent-lite` from Jupyter AI Lite. [Try it in the browser](https://jupyter-ai-contrib.github.io/jupyter-ai-pi-lite/lab/index.html).
- [jupyterlab-codex](https://github.com/oy-ilho/jupyterlab-codex) 🟡 - Codex CLI in a sidebar, with a server extension to keep the session alive.
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
- [GRAPHIT](https://github.com/Barbarossa2711/GRAPHIT) 🟢 - Tutoring system that models a lecture as a knowledge graph, with a tutor chat that answers only from the lecture slides, generated quizzes and a mastery score per concept that schedules reviews. Built for one German master's course, it runs with its own backend and JupyterHub through Docker Compose.
- [AI-ssignment](https://github.com/EtienneMueller/ai-ssignment) 🟢 - Shows under each question of an assignment notebook what a student who only uses AI would hand in, and the grade a model gives it. The simulated student pastes one question, pastes the whole notebook or works as an agent that runs code, and the notebooks follow nbgrader conventions. There is no release yet, so it installs from source.
- [FlowBook](https://github.com/stephenfreund/FlowBook) 🟢 - Marks cells whose inputs have changed, so re-running any cell gives the same answer as a top to bottom run. For each violation it reports, it can ask an LLM to diagnose the cause and offer one-click fixes. Without an API key the LLM part is off and the rest still works.
- [CRANE-LLM](https://github.com/PELAB-LiU/crane_llm) 🟢 - Research extension that predicts and diagnoses notebook crashes with any OpenAI compatible model, Gemini and a local Ollama included. Built-in checks catch the crashes that are certain from the live kernel state without calling the model, and can stop such a cell before it runs.
- [jupyter-geoagent](https://github.com/geojupyter/jupyter-geoagent) 🟢 - Map explorer for STAC catalogs with an MCP query interface over DuckDB, and reproducible exports of what the agent did.
- [GeoCopilot](https://pypi.org/project/opengeolab-geocopilot/) 🟢 - Codex-powered notebook agent for geospatial work, on top of `jupyter-server-mcp`. MIT, no public repository.
- [ClimateClaw for JupyterLite AI](https://github.com/freva-org/freva-web-nextgen/tree/main/packages/jupyterlite-climateclaw) 🟢 - Provider for JupyterLite AI that connects its chat to ClimateClaw, DKRZ's assistant for climate data on a Freva portal. Code that ClimateClaw runs on the portal is added to the open notebook with its output and figures, and signing in needs a Freva account.
- [oceanumlab](https://github.com/oceanum-io/oceanumlab) 🟢 - Panel for the Oceanum.io ocean data platform, with Datamesh datasets you drag into a cell as loading code and an AI chat that writes cells into the open notebook and can run them and read the output back. The data and the chat need an Oceanum.io account.
- [InstrMCP](https://github.com/caidish/instrMCP) 🟢 - MCP server suite that lets a model read QCodes instruments and measurement databases from a JupyterLab session in a physics lab.
- [smarts.bio](https://github.com/smartsbio/smarts-bio-jupyterlab) 🟢 - Bioinformatics agent that runs GPU pipelines such as RFdiffusion and Boltz, searches NCBI, UniProt and PDB, and opens FASTA, BAM, VCF and PDB files natively. Commercial, with an MIT wrapper package ([smarts.bio](https://smarts.bio)).
- [Lightcone Lab](https://github.com/LightconeResearch/jupyterlab-lightcone) 🟢 - Research workbench that connects analyses, cited papers and materialised outputs, with optional Jupyter AI integration.
- [SageMaker GenAI extension](https://pypi.org/project/sagemaker-gen-ai-jupyterlab-extension/) 🟢 - Amazon Q Developer chat panel for SageMaker Studio, which SageMaker Distribution 4.4 and later still installs but switches off in favour of Jupyter AI with the Kiro agent. Apache-2.0, with a required dependency under the Amazon Software License, and no public repository.
- [Xavier](https://github.com/CHI25-Xavier/Xavier) 🟡 - Research prototype from a CHI'25 paper on tabular data wrangling. It keeps the data in view while it suggests code. [Paper](https://doi.org/10.1145/3706598.3714239), [video](https://youtu.be/KTnCHSv1heI).
- [Auto Dashboards](https://github.com/orbrx/auto-dashboards) 🟡 - Turns a notebook into a Streamlit, Dash or Solara dashboard and previews it beside the notebook.
- [WWC Copilot](https://github.com/adamisom/jupyterlab-research-assistant-wwc-copilot) 🟡 - Academic research library with Semantic Scholar and OpenAlex import, PDF parsing and AI metadata extraction.
- [LLM Attributor](https://github.com/poloclub/LLM-Attributor) ⚪ - Georgia Tech widget that attributes generated text back to training data.
- [hintbot](https://github.com/educational-technology-collective/hintbot) ⚪ - Asks for a hint on the current cell in a teaching setting, and logs the request.

<table>
<tr>
<td width="33%"><a href="https://github.com/smartsbio/smarts-bio-jupyterlab"><img src="https://smarts-public.s3.us-east-1.amazonaws.com/jupyterlab/screenshot-structure-chat.png" alt="a protein structure answered in the chat"></a><br><sub><b>smarts.bio</b>: a protein structure answered in the chat</sub></td>
<td width="33%"><a href="https://github.com/Barbarossa2711/GRAPHIT"><img src="https://raw.githubusercontent.com/Barbarossa2711/GRAPHIT/main/docs/screenshots/overview.png" alt="a lecture as a concept tree, with mastery and the reviews that are due"></a><br><sub><b>GRAPHIT</b>: a lecture as a concept tree, with mastery and the reviews that are due</sub></td>
<td width="33%"><a href="https://github.com/CHI25-Xavier/Xavier"><img src="https://raw.githubusercontent.com/CHI25-Xavier/Xavier/master/assets/UI_Overview.png" alt="data kept in view while code is suggested"></a><br><sub><b>Xavier</b>: data kept in view while code is suggested</sub></td>
</tr>
</table>

## Building blocks

Plugins and libraries to build on. Few of them do anything on their own, and Jupyter AI v3 is assembled from them: installing `jupyter-ai` installs nine of the packages below, and its extras install six more. Every AI package in [jupyter-ai-contrib](https://github.com/jupyter-ai-contrib) is listed somewhere in this file, most of them here.

### Jupyter AI plugins

- [🪐 jupyter-ai-persona-manager](https://github.com/jupyter-ai-contrib/jupyter-ai-persona-manager) 🟢 - Registry that turns a class into a named participant in a chat.
- [🪐 jupyter-ai-jupyternaut](https://github.com/jupyter-ai-contrib/jupyter-ai-jupyternaut) 🟢 - Jupyternaut, the default persona, and the reference for writing another.
- [🪐 jupyter-ai-router](https://github.com/jupyter-ai-contrib/jupyter-ai-router) 🟢 - Routes each chat message to a persona.
- [🪐 jupyter-ai-litellm](https://github.com/jupyter-ai-contrib/jupyter-ai-litellm) 🟢 - Model abstraction over LiteLLM. This is how v3 connects to a model provider.
- [🪐 jupyter-ai-acp-client](https://github.com/jupyter-ai-contrib/jupyter-ai-acp-client) 🟢 - Agent Client Protocol client, the piece that lets external agents appear in the chat.
- [🪐 jupyter-ai-claude-code](https://github.com/jupyter-ai-contrib/jupyter-ai-claude-code) 🟡 - Jupyter AI persona that runs Claude Code.
- [🪐 jupyter-ai-personas](https://github.com/jupyter-ai-contrib/jupyter-ai-personas) ⚪ - Example personas for Jupyter AI v2, kept for reference.
- [🪐 jupyter-ai-chat-commands](https://github.com/jupyter-ai-contrib/jupyter-ai-chat-commands) ⚪ - Slash commands in the chat input.
- [🪐 jupyter-ai-tools](https://github.com/jupyter-ai-contrib/jupyter-ai-tools) 🟢 - Tool implementations for agents working on notebooks and files.
- [🪐 jupyter-ai-magic-commands](https://github.com/jupyter-ai-contrib/jupyter-ai-magic-commands) 🟢 - The v3 replacement for `jupyter-ai-magics`, built on LiteLLM.
- [jupyter-ai-manager](https://github.com/brichet/jupyter-ai-manager) 🟢 - Panel that installs Jupyter AI packages, such as Jupyternaut and the ACP client, and the npm or pip packages that connect agents such as Claude Code and Codex over ACP. A new agent appears in the chat without a server restart, and the panel installs from source until a release is published.
- [🪐 jupyter-ai-demos](https://github.com/jupyter-ai-contrib/jupyter-ai-demos) ⚪ - Notebooks and custom personas demonstrating what Jupyter AI v3 can do. Read the personas before writing your own.

### Chat and notebook UI

- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> Jupyter Chat](https://github.com/jupyterlab/jupyter-chat) 🟢 - The chat document, the React components and the `jupyterlab-chat` extension. Install it alone for a chat between humans, or depend on it to write your own assistant. [Try it on Binder](https://mybinder.org/v2/gh/jupyterlab/jupyter-chat/main?urlpath=lab).
- [🪐 jupyter-chat-components](https://github.com/jupyter-ai-contrib/jupyter-chat-components) 🟢 - Extra components to display inside a chat. [Try it in the browser](https://jupyter-ai-contrib.github.io/jupyter-chat-components/lab/index.html?path=components_demo.ipynb).
- [🪐 jupyter-floating-chat](https://github.com/jupyter-ai-contrib/jupyter-floating-chat) 🟡 - Chat input that floats over the document.
- [🪐 jupyterlab-diff](https://github.com/jupyter-ai-contrib/jupyterlab-diff) 🟢 - Cell and file diffs with several strategies, for showing what an agent proposes. [Try it in the browser](https://jupyter-ai-contrib.github.io/jupyterlab-diff/lab/index.html?path=diff-demo.ipynb).
- [🪐 jupyterlab-cell-input-footer](https://github.com/jupyter-ai-contrib/jupyterlab-cell-input-footer) 🟡 - A place under a cell input to put your own UI.
- [🪐 jupyterlab-ai-commands](https://github.com/jupyter-ai-contrib/jupyterlab-ai-commands) 🟢 - JupyterLab commands written for agents to call.
- [🪐 jupyterlab-commands-toolkit](https://github.com/jupyter-ai-contrib/jupyterlab-commands-toolkit) 🟢 - Exposes the JupyterLab command registry as an AI toolkit.
- [🪐 jupyterlab-notebook-awareness](https://github.com/jupyter-ai-contrib/jupyterlab-notebook-awareness) ⚪ - Publishes the current notebook and the active cell into the awareness state, so an agent can read where the cursor is.
- [🪐 jupyterlab-document-collaborators](https://github.com/jupyter-ai-contrib/jupyterlab-document-collaborators) ⚪ - Shows who else has the document open, along the top of it.
- [jupyterlab_voice_capture_extension](https://github.com/stellarshenson/jupyterlab_voice_capture_extension) 🟢 - Streams the browser microphone to a server side FIFO, so a CLI agent in a container can use voice mode.
- [Agent Runtimes](https://github.com/datalayer/agent-runtimes) 🟢 - Datalayer's agent server and React chat components, which Jupyter AI Agents is built on. It serves a Pydantic AI agent over ACP, AG-UI, A2A and the Vercel AI SDK, and installs as a Jupyter Server extension.

<table>
<tr>
<td width="60%"><a href="https://github.com/jupyterlab/jupyter-chat"><img src="https://raw.githubusercontent.com/jupyterlab/jupyter-chat/main/python/jupyterlab-chat/screenshot.gif" alt="the shared chat document Jupyter AI is built on"></a><br><sub><b>Jupyter Chat</b>: the shared chat document Jupyter AI is built on</sub></td>
</tr>
</table>

### Live reload

An agent writes to the notebook file while you have it open. By default JupyterLab keeps showing the old cells as reloading the document could lose the widget state. These extensions instead update the open document when the file changes.

- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> jupyter-collaboration](https://github.com/jupyterlab/jupyter-collaboration) 🟢 - Real time collaboration on Yjs. It is what lets two people, or a person and an agent, type into one notebook. Jupyter AI installs it under the `rtc` extra.
- [🪐 jupyter-live-content](https://github.com/jupyter-ai-contrib/jupyter-live-content) 🟢 - Live file content updates, so the UI follows an agent editing on disk.
- [🪐 jupyter-server-documents](https://github.com/jupyter-ai-contrib/jupyter-server-documents) 🟢 - Keeps document and kernel state on the server with pycrdt, for faster updates and lower memory. Jupyter AI installs it under the `rtc-jsd` extra.
- [Advanced Markdown Viewer](https://github.com/stellarshenson/jupyterlab_advanced_markdown_viewer_extension) 🟢 - Keeps the Markdown preview in step with the file while an agent writes it, with added text typed in on green and removed text struck through on red. Marks and notes are stored in the file as HTML comments, and a bundled agent skill lets the agent read and answer them.
- [hot-notebook-patching](https://github.com/kolibril13/hot-notebook-patching) 🟡 - Patches only the cells that changed, so the kernel keeps running and widgets keep their state. Written for notebooks edited by Claude Code.
- [jupyterlab-claude-code-refresh](https://github.com/wenatuhs/jupyterlab-claude-code-refresh) ⚪ - Reloads the open notebook from disk when Claude Code edits the file.

### MCP

An MCP server lets an agent that runs outside JupyterLab read and edit a notebook. It also lets an extension offer its own commands as tools.

- [Jupyter MCP Server](https://github.com/datalayer/jupyter-mcp-server) 🟢 - The most starred MCP server for Jupyter. Lets any MCP client read, write and run cells, including multimodal output.
- [jupyter-collab-mcp](https://github.com/lipa88/jupyter-collab-mcp) 🟢 - MCP server that joins the notebook open in your JupyterLab through `jupyter-collaboration`, so the agent's edits, cell runs and outputs appear in your tab while it works. It runs with `npx`, so nothing is installed into the Jupyter environment, and it can start your own JupyterHub server.
- [Agent Jupyter Toolkit](https://github.com/Cyb3rWard0g/agent-jupyter-toolkit) 🟢 - Python library and MCP server (`mcp-jupyter-notebook`) that run code in a local kernel or on a Jupyter server, and edit notebooks through `jupyter-collaboration` so the changes appear in your open JupyterLab tab. Optional tools run PostgreSQL and Azure Monitor Logs queries as notebook cells and keep the result in the kernel as a DataFrame.
- [true-python-mcp](https://github.com/Speretta/true-python-mcp) 🟢 - MCP server in one Rust binary that edits `.ipynb` and marimo notebooks cell by cell without touching the rest of the file, so the git diff shows only the edited lines, and lints, formats and type-checks them with ruff and ty built in. It starts no kernel and runs no code, and it refuses a write when the file changed since the agent read it.
- [cursor-notebook-mcp](https://github.com/jbeno/cursor-notebook-mcp) 🟡 - MCP server that edits `.ipynb` files for an agent that has no notebook UI of its own, written for Cursor.
- [🪐 jupyter-server-mcp](https://github.com/jupyter-ai-contrib/jupyter-server-mcp) 🟢 - Jupyter Server extension that registers Python functions as MCP tools from inside the server. Jupyter AI uses it.
- [jupyter-mcp-tools](https://github.com/datalayer/jupyter-mcp-tools) 🟢 - Exposes JupyterLab commands as MCP tools.
- [🪐 jupyter-mcp-manager](https://github.com/jupyter-ai-contrib/jupyter-mcp-manager) 🟢 - UI and backend for configuring which MCP servers are available to other extensions.
- [MCP Console](https://pypi.org/project/jupyterlab-mcp-console/) 🟡 - Discover, inspect and deploy MCP servers through an AgentRegistry API. BSD-3-Clause, no public repository.
- [🪐 jupyter-server-ai-tools](https://github.com/jupyter-ai-contrib/jupyter-server-ai-tools) ⚪ - Jupyter Server extension that collects the tools other extensions declare, so an agent can list them from one place.
- [JupyterLite WebMCP](https://github.com/alliecatowo/jupyterlite-web-mcp) 🟢 - Gives a browser agent 22 WebMCP tools to read, edit, run and comment on the notebook you have open, unsaved edits included. It has no server part, so it also works in JupyterLite, and it needs Chrome with WebMCP turned on or ChatGPT's in-app browser.
- [jupyter-webmcp](https://github.com/jtpio/jupyter-webmcp) 🟢 - Registers the commands of a JupyterLab, Notebook 7 or JupyterLite page as WebMCP tools, so a browser agent can open, edit and run notebooks, answer dialogs and run any other command. It has no server part and needs Chrome with WebMCP turned on or ChatGPT's in-app browser. [Try it in the browser](https://jtpio.github.io/jupyter-webmcp/lab/index.html?path=demo.ipynb).

<table>
<tr>
<td width="33%"><a href="https://github.com/datalayer/jupyter-mcp-tools"><img src="https://images.datalayer.io/products/jupyter-mcp-tools/jupyter-mcp-tools.gif" alt="JupyterLab commands called as MCP tools"></a><br><sub><b>jupyter-mcp-tools</b>: JupyterLab commands called as MCP tools</sub></td>
<td width="33%"><a href="https://github.com/jupyter-ai-contrib/jupyter-mcp-manager"><img src="https://raw.githubusercontent.com/jupyter-ai-contrib/jupyter-mcp-manager/main/MCP-manager-settings-panel.png" alt="choosing which MCP servers are available"></a><br><sub><b>jupyter-mcp-manager</b>: choosing which MCP servers are available</sub></td>
<td width="33%"><a href="https://github.com/jtpio/jupyter-webmcp"><img src="https://raw.githubusercontent.com/jtpio/jupyter-webmcp/main/screenshot.png" alt="the ChatGPT desktop app creating and running a notebook in JupyterLite"></a><br><sub><b>jupyter-webmcp</b>: the ChatGPT desktop app creating and running a notebook in JupyterLite</sub></td>
</tr>
</table>

## IPython

These extend IPython, which runs the code in a Python notebook, instead of JupyterLab. Magics work the same in a notebook and in a terminal IPython session.

- [ipyai](https://github.com/AnswerDotAI/ipyai) 🟢 - Terminal IPython in which code, shell commands and prompts to Codex or Claude share one transcript, so each prompt sees the cells and outputs before it. Sessions save to `.ipynb`, and the kernels come from a local rustygate gateway, a proprietary binary from the same team. Apache-2.0 in `pyproject.toml`, but the repository has no LICENSE file.
- [ipyllm](https://github.com/juampatronics/ipyllm) 🟢 - Magics `%llm` and `%%llm` that let any model of the `llm` package, local Ollama models included, list and inspect your variables, read the input history and run code in the kernel. The model runs code without asking unless you turn on approval, and `%%llm --run` asks it to explain the output of a shell command.
- [jupyter-ext-ai](https://github.com/novatechnolab/jupyter-ext-ai) 🟡 - Magic commands for chatting with OpenAI, Gemini and Claude from a cell.
- [genai](https://github.com/rgbkrk/genai) ⚪ - IPython magics that read your error and your dataframes before suggesting a fix. Written at Noteable, a notebook company that later shut down.

## Beyond the JupyterLab UI

These are not JupyterLab extensions. They are command line tools, kernels, agent plugins and models that a notebook user runs next to Jupyter.

- [🪐 nb-cli](https://github.com/jupyter-ai-contrib/nb-cli) 🟢 - Command line for notebooks with an AI-optimised markdown format, so an agent can work without a browser.
- [jupyter-jcli](https://github.com/TTTPOB/jcli) 🟢 - CLI that lets Claude Code, Codex or OpenCode run cells in a kernel on your Jupyter server and saves the outputs into the notebook. The agent edits a paired `.py` file in py:percent format, while hooks installed by `j-cli setup` stop direct `.ipynb` edits and keep the two files in sync.
- [nblean](https://github.com/kaanrkaraman/nblean) 🟢 - CLI and agent skill that show a coding agent a notebook as one line per cell, with long outputs clipped and plots saved as files, so the agent reads less. Cells run in a kernel that stays alive between commands, and their outputs are saved into the `.ipynb`.
- [notebook-to-pipeline](https://github.com/Abelo9996/notebook-to-pipeline) 🟢 - CLI, MCP server and agent skill that turn a notebook into a Python package, with a test that the package gives the same variables and figures as a fresh run of the notebook. With `--refactor` it calls Claude Code or Codex to split the package into stages, and rejects any pass that changes an output.
- [Encore](https://github.com/catalystneuro/encore) 🟢 - CLI from CatalystNeuro in which Claude Code agents read a paper, write down its claims and test them on the paper's dataset in Jupyter notebooks, for a local directory, files at a URL or a dataset in the DANDI Archive. The report gives the outcome of each claim and the problems found in the data, such as units that do not match or metadata that is missing.
- [pydantic-ai-kernel](https://github.com/mariusgarenaux/pydantic-ai-kernel) 🟢 - A kernel that runs a Pydantic AI agent, so each cell is a message and the reply streams back as output, in JupyterLab, Notebook or `jupyter console`. Magics configure the agent, its MCP servers and its tools, and a tool call can wait for your approval.
- [opencode-ipynb](https://github.com/Restodecoca/opencode-ipynb) 🟢 - OpenCode plugin with tools that inspect, read, edit, run, clean and export `.ipynb` files one cell at a time, with a local kernel that can stay warm between calls and outputs saved into the notebook. Version 2 needs OpenCode 2, and version 0.1 is the one for OpenCode 1.
- [jupyterlab-cli](https://github.com/wenmin-wu/jupyterlab-cli) 🟡 - CLI where every command is one HTTP call to the server, plus clipboard and context helpers in the UI.
- [agent-client-kernel](https://github.com/wiki3-ai/agent-client-kernel) 🟡 - A kernel that connects to an agent over the Agent Client Protocol, so the agent answers your cells wherever a kernel can run.
- [jupyter-agents-kit](https://github.com/p4ulbr4dl3y/jupyter-agents-kit) 🟡 - Small fine-tuned models for JupyterLab cell manipulation, with datasets published.
- [Elyra](https://github.com/elyra-ai/elyra) 🟢 - Runs notebooks as pipelines on Kubeflow Pipelines and Apache Airflow, and predates the LLM extensions. It is still the largest set of JupyterLab extensions for machine learning work.

## Agent skills

A skill is a `SKILL.md` file of instructions that a coding agent such as Claude Code, Codex or GitHub Copilot reads when a task matches it. Some come with an extension or a script, and the rest are only instructions.

- [notebook-guidance (Google Cloud)](https://github.com/GoogleCloudPlatform/data-agent-kit-plugin/tree/main/skills/notebook-guidance) 🟢 - Skill from Google's Data Agent Kit plugin that tells the agent when an analysis needs a notebook, how to choose and check its kernel, and to write, run and check one cell at a time when it can run cells. Queries go to BigQuery through its `%%bqsql` magic, so it needs a Google Cloud account.
- [skore-skills](https://github.com/probabl-ai/skore-skills) 🟢 - Skills from probabl, the company founded by the creators of scikit-learn, that take a machine learning project from data exploration to an audit with scikit-learn, skrub and skore. The agent works in jupytext `# %%` files and writes the `.ipynb` notebooks and HTML viewers from them. The repository has an eval of the skills on small and large models.
- [xtralab skills](https://github.com/jtpio/xtralab/tree/main/agent-skill/skills) 🟢 - Skills from xtralab that change JupyterLab settings, such as the theme, the sidebar tabs and the enabled extensions, or walk you through code by opening files and highlighting lines in your JupyterLab tab. Two more start and stop xtralab from the terminal, and the xtralab plugin for Claude Code installs all four.
- [jupyterlite (Galaxy)](https://github.com/galaxyproject/galaxy-skills/tree/main/skills/galaxy-integration/jupyterlite) 🟢 - Skill from the Galaxy Project for writing JupyterLite notebooks that read and write the datasets of a Galaxy history in the browser with the `gxy` package, for plotting, reshaping and inspection that a Galaxy tool does not cover. It comes with four example notebooks.
- [iterative-data-science](https://github.com/NguyenTran2002/iterative-data-science) 🟢 - Claude Code skill that makes the agent add one to three cells at a time, run them and read the output, and save and open each figure before it writes the next section. The repository publishes five pairs of runs of the same analysis with and without the skill, with every log and notebook.
- [jupytermind](https://github.com/nahisaho/jupytermind) 🟢 - GitHub Copilot skills that run cells through Jupyter MCP Server for data analysis, chemistry, genomics, materials science and structural biology, and write each conclusion into the notebook next to the cell that supports it. The Python helpers install from npm and set up their own virtual environment on first use.
- [paper-lab](https://github.com/olyamasaeva/paper-lab) 🟢 - Claude Code skill that turns a paper, an arXiv id or lecture slides into a Jupyter assignment, where you implement the paper's method in stub functions and check it against tests and the paper's own numbers. The notebooks carry nbgrader metadata, and the repository has worked examples with solved copies.
- [<img src="https://raw.githubusercontent.com/jupyter/design/main/logos/Favicon/favicon.svg" height="14" alt="Project Jupyter"> Plugin Playground](https://github.com/jupyterlab/plugin-playground) 🟡 - Extension for writing JupyterLab plugins inside JupyterLab and loading them without a rebuild, with a skill that tells an agent how to write a plugin and load it through the playground's commands. With Jupyter AI Lite installed, a command from the Commands tab can be sent to the chat, so the model picks where to insert it. [Try it in the browser](https://jupyterlab-plugin-playground.readthedocs.io/en/latest/lite/lab/).
- [jupyter-notebook (OpenAI)](https://github.com/openai/skills/tree/main/skills/.curated/jupyter-notebook) 🟡 - Codex skill from OpenAI's curated set that creates and edits notebooks from experiment and tutorial templates, with a script that writes the `.ipynb` so the agent does not write notebook JSON by hand. JetBrains, Letta and Microsoft's agents course ship copies of it.

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) first. It has the listing criteria, including what is deliberately left out, how an entry gets its marker, and how the list was assembled.

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related or neighboring rights to this work.
