# Contributing

Thanks for taking the time. A pull request that adds one extension is the most useful kind. The sections on markers, screenshots, icons and how the list was assembled carry dates, because those claims go stale. Recheck anything whose date has aged.

## Listing criteria

An entry has to install into JupyterLab or Jupyter Notebook 7, as a front end extension, a server extension, or both, and it has to call an AI model. Language models are most of it, but speech, image and in-browser models count too. A kernel, a CLI or an MCP server can go under *Beyond the JupyterLab UI* if a notebook user runs it next to Jupyter, and an IPython magic or extension goes under *IPython*. An agent skill goes under *Agent skills* when its instructions are about working with notebooks or JupyterLab.

What is deliberately left out:

- **Forks of JupyterLab.** [Pretzel](https://github.com/pretzelai/pretzelai) and [Jupyter Studio](https://github.com/deepelementlab/jupyter-studio) rewrite or vendor the application, so you cannot add them to a lab you already run. Pretzel has not been updated since September 2024, and Jupyter Studio ships a copy of the JupyterLab source tree and an Electron shell.
- **Rebadged copies.** Some PyPI packages ship another project's extension under a new name. `ghn-jupyter-ai` has Jupyter AI's own metadata and declares the `@jupyter-ai/core` extension path. `jupyterlab-khulnasoft` is `jupyterlab-codeium` with the vendor name swapped. Domain forks that do change something, such as [dkrz-jupyter-ai](https://github.com/freva-org/dkrz-jupyter-ai) for climate work, are left out for a different reason: install the upstream and add what you need.
- **Closed-source packages.** A few extensions install from PyPI under a licence that forbids copying, modification or use, and one ships compiled `.pyc` and `.so` files with no Python source at all. They are left out because a reader cannot check what runs in their browser and their kernel, cannot fix it, and cannot fork it if the vendor stops. A missing `LICENSE` counts the same way: with no grant, there is no permission. Read the licence in the wheel before adding anything, since the PyPI classifier is self-declared and several packages claim an OSI licence while shipping a copyright line and nothing else.
- **Packages whose source is gone.** `ai-einblick-prompt` (Einblick, acquired in 2023), `jupytergpt` (`EasonC13/JupyterGPT`) and `notebook-ai` (`nikhilk/nbai`) still install from PyPI, and every repository they name returns 404. MutableAI's own repository is gone too; the only surviving copy is [orchest/jupyterlab_mutableai_optin](https://github.com/orchest/jupyterlab_mutableai_optin), last touched in 2022.

## How to write the entry

```
- [Name](https://github.com/owner/repo) 🟢 - What it adds, in one or two sentences.
```

Say what the extension does for the person using it. "Adds an Explain button to the cell toolbar" tells the reader something. "AI-powered assistant leveraging LLMs" tells them nothing. Start the description with a capital letter and end it with a period. Keep it to two sentences.

Do not put a date in an entry. The dot gives the age and the badges in the At a glance table are live, so a written date only goes stale. Dates belong in this file, next to the claim they support.

Put the entry in the section that matches what the extension does, and give it a marker from the date of the last commit ([Markers](#markers) has the method). Within a section, order is roughly active first and then by how much the project is used. Do not list a project twice, and do not link the same repository from two entries. A section has up to three screenshots or screencasts, and [Screenshots and screencasts](#screenshots-and-screencasts) has the rules for them.

## Markers

The marker is a coloured dot after the project name, and it comes from the date of the last commit on the default branch:

| Marker | Name | Last commit |
| --- | --- | --- |
| 🟢 | active | Within 4 months |
| 🟡 | maintained | Within 12 months |
| ⚪ | quiet | 1 to 2 years ago |

Older than that, or archived, or the model service behind it is gone: the entry belongs in [HISTORICAL.md](HISTORICAL.md).

Read the date from the GitHub API. A date written in a readme goes stale, and pushes to side branches and Dependabot commits make a repository look busier than it is:

```bash
gh api repos/OWNER/REPO/commits?per_page=1 --jq '.[0].commit.committer.date'
```

Use that field. `pushed_at` counts pushes to side branches, so it runs ahead of the work. A repository whose recent traffic is all Dependabot counts as quiet, so check what the commits are. For a project with no public repository, use the latest PyPI release date instead, and say so in the entry. Read the licence out of the wheel while you are there, because that is what decides whether it belongs in the list at all.

Four months is the line for active because this is a small ecosystem, and a working extension can go a release cycle without a commit.

The two year line was set on 2026-09-22. Recheck it when JupyterLab 5 is released. JupyterLab 4.0 was released on 2023-05-15, 4.6.4 was current on that date, and there has been no breaking release in between. An extension whose last commit was in 2025 therefore usually still installs and runs, so the list waits two years before calling anything dormant. When 5.0 is released, every extension pinned to `jupyterlab<5` stops installing on the current version, and that date becomes a better line than any fixed interval. Move the threshold then, and say so here.

Sections group extensions by what they do, and the date is a marker on the entry. The two axes were tried the other way round first, with activity as the sections and themes inside the newest one. It reads badly: someone asking which extension gives them inline completion has to scan every section, and the thematic split applies to one section only. Theme first, date as a marker, keeps both readable.

## Screenshots and screencasts

Up to three per section, in an HTML table right after the list, each one linked to its project and captioned with what it shows. Use a screencast when the project has one and a screenshot when it does not.

Check two things before embedding an image. A `github.com/user-attachments/...` asset renders only in the repository it was uploaded to, so it cannot be embedded here: use a file from the repository tree instead. And check the byte size: several demo GIFs in this field are 4 to 20 MB. That is fine in their own readme and too heavy for a page with a dozen of them, so link those instead of embedding them.

Resolve a relative path in someone's readme against their default branch.

## Icons

The Jupyter logo mark is for a project maintained by Project Jupyter, in one of its official GitHub organisations. In the readme that is `jupyterlab`, but `jupyterlite`, `jupyter`, `jupyterhub`, `jupyter-book` and the other official organisations count the same way. The [list of subprojects](https://jupyter.org/governance/list_of_subprojects.html) settles it. Do not give the mark to anything else, however official it looks.

The planet is for [jupyter-ai-contrib](https://github.com/jupyter-ai-contrib), a community organisation that is not under Project Jupyter governance. Every AI package in that organisation is listed somewhere in the readme. On 2026-10-22 it had 31 repositories, and four are left out: `ipykernel-uv`, a kernel that does not call a model, `jupyter-ai-devrepo`, a developer checkout of the other packages, and `.github` and `team-compass`, which are not packages.

The second marker is an emoji because the two logo variants in `jupyter/design` are indistinguishable at 14 pixels, and the monochrome one disappears on GitHub's dark theme.

## Adding your own project

That is fine, and normal. Say in the pull request that it is yours. A project that has been public for less than a month, or that has no readme explaining how to install it, will be asked to wait.

## Removing an entry

Open an issue if a project has moved, been renamed, or started requiring an account it did not need before. Renames are common here, and several entries have already changed owner.

## How the list was assembled

Written 2026-09-22.

The starting point is PyPI, because most JupyterLab extensions are never announced anywhere and a search finds only the ones that were. Four classifiers cover the field:

- `Framework :: Jupyter :: JupyterLab :: Extensions :: Prebuilt`
- `Framework :: Jupyter :: JupyterLab :: Extensions`
- `Framework :: Jupyter :: JupyterLab :: 4`
- `Framework :: Jupyter :: JupyterLab :: 3`

Their union was 1234 projects. Each one was read twice, because either pass alone misses a whole class of extension:

1. The summary was grepped for AI terms (ai, llm, gpt, claude, copilot, agent, agentic, chat, prompt, completion, mcp and so on). That gave 125 candidates.
2. The `requires_dist` list was grepped for model SDKs (`openai`, `anthropic`, `litellm`, `langchain`, `langgraph`, `mcp`, `ollama`, `claude-agent-sdk`, `transformers`, `pydantic-ai`, `deepagents`). That gave 49, and it catches the packages whose summary does not mention AI.

Those four classifiers are not the whole field. `Framework :: Jupyter` returned 2753 projects and `Framework :: Jupyter :: JupyterLab` returned 1338, and 1581 of those have neither an Extensions nor a version classifier, so the first pass never saw them. Sweeping that set the same way found four more entries, including a 2021 Codex extension with 92 stars. Browse the parent classifiers as well when you redo this.

PyPI alone is not enough, so four more passes ran on top:

- npm keyword search on `jupyterlab-extension` crossed with ai, llm, chat, agent, copilot, completion, assistant and gpt.
- GitHub repository search and topic search (`topic:jupyterlab-extension` with `topic:ai` and `topic:llm`).
- GitHub code search for `IInlineCompletionProvider` and `registerInlineProvider`. This finds completion providers whatever the package is called.
- Full repository listings for the `jupyter-ai-contrib`, `jupyterlab`, `jupyterlite` and `datalayer` organisations.

Licence and content claims come from reading the wheel. A badge and a classifier are both self-declared. Several packages have an OSI classifier and a `LICENSE` file with no grant in it, and one has compiled `.pyc` and `.so` files only. When the readme calls a package closed source, quote the file that shows it.

To redo the PyPI pass, list the classifier index and read each project's metadata from `https://pypi.org/pypi/<name>/json`. Do not install anything to inspect it: read the wheel with `zipfile`, so the package's code never runs.
