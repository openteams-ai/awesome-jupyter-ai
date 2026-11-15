# Historical

> Jupyter AI extensions that are no longer worked on, kept because the ideas in them are still worth reading.

These are split out of the [main list](README.md), which covers anything with a commit in the last two years. JupyterLab has not had a breaking release since 4.0 in May 2023, so several of these still install; nobody is fixing them if they do not.

## Contents

- [Dormant](#dormant)
- [Archived or discontinued](#archived-or-discontinued)

## Dormant

No commit for over two years. These were written against the first generation of chat APIs.

- [Chapyter](https://github.com/chapyter/chapyter) - The best known of the 2023 generation: a `%%chat` magic that writes the code and runs it, with history and an undo. Worth reading for the design.
- [Lightrail](https://github.com/lightrail-ai/lightrail) - Cross-application AI command bar with a JupyterLab connector.
- [JupyterLab Codex (lhr0909)](https://github.com/lhr0909/jupyterlab-codex) - The first of them: a 2021 extension against the original Codex private beta.
- [gpt-jupyterlab](https://github.com/henshinger/gpt-jupyterlab) - Text and code completion on cells through the OpenAI API.
- [jupyter_plz](https://github.com/Akramz/jupyter_plz) - `%plz` a request and get the code.
- [jupyterlab-transformers-completer](https://github.com/krassowski/jupyterlab-transformers-completer) - Inline completion from transformers.js, running in the browser with no server. [Try it on Binder](https://mybinder.org/v2/gh/krassowski/jupyterlab-transformers-completer/main?urlpath=lab).
- [gpt-magic](https://github.com/biff-ai/gpt-magic) - GPT magic commands for a cell.
- [codex-chat-notebook](https://github.com/oeway/codex-chat-notebook) - Data science by chat, written against the original OpenAI Codex.
- [LabPilot](https://github.com/aleksanderhan/labpilot) - Refactor, debug, explain and a semi-autonomous mode, each with its own demo GIF.
- [JupyterLab-CodeGen](https://archive.softwareheritage.org/browse/origin/directory/?origin_url=https://github.com/thaitran/JupyterLab-CodeGen) - Cell code generation with GPT-4. The GitHub repository was deleted, so the link goes to the copy in Software Heritage.
- [jupyterlab-starchat-extension](https://github.com/aolney/jupyterlab-starchat-extension) - Interface to the StarChat open model, from the brief window when that was the open alternative.
- [jupylot](https://github.com/vrvrv/jupylot) - Error checking assistant.
- [Notebook Copilot](https://github.com/talperetz/notebook-copilot) - `%copilot` magic that writes a whole notebook, code and markdown, from a description of the goal. Reads the cells already there for context. Last worked on in 2023.
- [chatlab](https://github.com/rgbkrk/chatlab) - Library for trying out tool calling in a notebook, with the model able to call functions you defined in the cell above.
- [CoML](https://github.com/microsoft/CoML) - Microsoft Research assistant with three modes, including one that suggests what to try next on a machine learning task. The readme has demo GIFs.

<table>
<tr>
<td width="33%"><a href="https://github.com/aleksanderhan/labpilot"><img src="https://raw.githubusercontent.com/aleksanderhan/labpilot/main/docs/refactor.gif" alt="refactoring a cell, 2023"></a><br><sub><b>LabPilot</b>: refactoring a cell, 2023</sub></td>
<td width="33%"><a href="https://github.com/biff-ai/gpt-magic"><img src="https://raw.githubusercontent.com/biff-ai/gpt-magic/main/GPTMagic.gif" alt="a GPT magic command, 2023"></a><br><sub><b>gpt-magic</b>: a GPT magic command, 2023</sub></td>
<td width="33%"><a href="https://github.com/microsoft/CoML"><img src="https://raw.githubusercontent.com/microsoft/CoML/main/assets/demo_coml.gif" alt="a magic that fills in the next step, 2023"></a><br><sub><b>CoML</b>: a magic that fills in the next step, 2023</sub></td>
</tr>
</table>

## Archived or discontinued

The repository is read-only, or the model service behind it has been switched off.

- [Qiskit Code Assistant](https://github.com/Qiskit/qiskit-code-assistant-jupyterlab) - Inline completion trained on Qiskit. IBM retired the hosted service on 29 May 2026 and archived the repository, but the extension still works against a local Ollama model or an OpenAI compatible endpoint.
- [tabnine-jupyterlab](https://github.com/codota/tabnine-jupyterlab) - Tabnine's client, from before JupyterLab had an inline completion API. Archived, last commit 2021.
- [icortex](https://github.com/textcortex/icortex) - A kernel, so every cell works this way: natural language in, Python out, with the generated code kept in the notebook. Archived.
- [jupyter-voicepilot](https://github.com/JovanVeljanoski/jupyter-voicepilot) - Whisper plus GPT-3, so you could talk to the notebook in 2023. Archived.
- [jupyai](https://github.com/ploomber/jupyai) - Ploomber's experiment in adding AI to JupyterLab. Archived.
- [jupyterlab-codeium](https://github.com/jtpio/jupyterlab-codeium) - Codeium through the inline completion API. Archived after Codeium became Windsurf.
- [codeium.jupyter](https://github.com/Exafunction/codeium.jupyter) - Codeium's own JupyterLab client. It had no commit after Codeium became Windsurf, and the repository is now archived.
- [Sage Agent](https://pypi.org/project/sage-agent-internal/) - Notebook assistant. Its default model proxy no longer answers, and the vendor now publishes it as SignalPilot under a proprietary licence. BSD-3-Clause, no public repository.
