# SOP: Build an Obsidian LLM-Wiki Based on Karpathy's LLM Wiki Idea

## Purpose

This SOP guides a human and an AI agent through building an Obsidian vault that works as an LLM-maintained personal wiki.

The workflow is based on Karpathy's idea of using an LLM to maintain a long-lived Markdown wiki instead of only answering one-off questions from uploaded files.

## Final Outcome

At the end of this workflow, the human should have:

- An Obsidian vault with a clean LLM-Wiki structure.
- A `raw/` area for source material.
- A `wiki/` area for long-lived synthesized knowledge.
- Templates for concepts, sources, and projects.
- Prompts for ingesting sources, creating pages, and linting the wiki.
- An `AGENTS.md` file that tells AI agents how to maintain the vault.
- Recommended Obsidian plugins installed or documented.
- Optional GitHub backup through Obsidian Git.

## When To Use This SOP

Use this SOP when:

- You want Obsidian to become a structured knowledge base.
- You want AI agents to maintain Markdown knowledge pages over time.
- You want to separate raw source material from synthesized knowledge.
- You want a repeatable workflow for future research topics.

Do not use this SOP when:

- You only need a one-time article summary.
- You do not want AI to write or reorganize files.
- Your vault contains highly sensitive content that should not be processed by AI.

## Human Preparation

Before the AI agent starts, the human should prepare:

- The target Obsidian vault path.
- The intended vault name.
- A decision on whether GitHub backup should be private or public.
- GitHub login through `gh` or another Git client, if GitHub backup is needed.
- Obsidian installed locally.
- Optional browser Web Clipper installed.
- A small first topic or source set for testing.

Recommended human decisions:

```text
Vault path: /Users/<user>/Documents/obsidian/wiki
GitHub repository: <github-user>/wiki
Repository visibility: private
First test topic: Karpathy LLM Wiki
```

## Inputs For The AI Agent

The human should provide:

```text
Target Obsidian vault path:
GitHub repository name, if needed:
Repository visibility:
Whether to initialize git:
Any existing files that must not be changed:
```

If the human does not specify visibility for a personal knowledge vault, the AI should default to private.

## AI Execution Plan

### 1. Inspect Current State

The AI should check:

- Whether the target vault path exists.
- Whether `.obsidian/` exists.
- Whether the vault already contains user notes.
- Whether there is a nested duplicate path, such as `wiki/wiki`.
- Whether git is already initialized.
- Whether required plugins are installed or enabled.

Useful checks:

```bash
ls -la <vault-path>
find <vault-path> -maxdepth 2 -type d
find <vault-path>/.obsidian -maxdepth 3 -type f
git -C <vault-path> status --short
git -C <vault-path> remote -v
```

### 2. Create The LLM-Wiki Structure

Create this structure inside the vault:

```text
raw/
  articles/
  books/
  papers/
  clips/
  meetings/

wiki/
  concepts/
  people/
  projects/
  books/
  topics/
  comparisons/

templates/
prompts/
docs/
```

The AI should only create missing directories and should not remove existing user files.

### 3. Create Core Files

Create these files:

```text
LLM-Wiki 入口.md
AGENTS.md
index.md
log.md
资料处理看板.md
raw/README.md
wiki/README.md
docs/Karpathy LLM Wiki 与 Obsidian 知识库结合.md
docs/Obsidian 插件建议.md
templates/concept-template.md
templates/source-template.md
templates/project-template.md
prompts/ingest-source.md
prompts/lint-wiki.md
prompts/create-page.md
wiki/concepts/LLM-Wiki.md
wiki/topics/Obsidian 与 LLM 知识库.md
wiki/comparisons/RAG-vs-LLM-Wiki.md
```

### 4. Configure Obsidian Templates

If Obsidian's core Templates plugin is enabled, create:

```text
.obsidian/templates.json
```

Recommended content:

```json
{
  "folder": "templates",
  "dateFormat": "YYYY-MM-DD",
  "timeFormat": "HH:mm",
  "templateTrigger": "{{",
  "templateEndTrigger": "}}"
}
```

### 5. Document Recommended Plugins

The AI should document these plugins:

- Web Clipper: captures web pages into `raw/articles/`.
- Dataview: builds dashboards and dynamic indexes.
- Omnisearch: improves search across the vault.
- Obsidian Git: commits and pushes vault changes.

The AI can inspect whether plugins are installed by checking:

```text
.obsidian/community-plugins.json
.obsidian/plugins/<plugin-id>/manifest.json
```

Expected plugin IDs:

```text
dataview
omnisearch
obsidian-git
```

Web Clipper may exist as a browser extension and may not be fully visible from the vault files.

### 6. Initialize Git And GitHub Backup

If the human asks for GitHub backup:

1. Check `gh auth status`.
2. Check whether the target GitHub repository already exists.
3. Create a private repository unless the human asks for public.
4. Initialize git if needed.
5. Add a `.gitignore`.
6. Commit the vault.
7. Add `origin`.
8. Push `main`.

Recommended `.gitignore`:

```gitignore
.DS_Store
.obsidian/workspace.json
.obsidian/workspace-mobile.json
.obsidian/cache/
.obsidian/plugins/*/cache/
.obsidian/plugins/*/.cache/
.trash/
*.tmp
*.bak
```

Recommended first commit:

```text
Initial Obsidian wiki vault
```

### 7. Verify The Result

The AI must verify:

- `LLM-Wiki 入口.md` exists.
- `.obsidian/` exists in the vault root.
- `raw/`, `wiki/`, `docs/`, `prompts/`, and `templates/` exist.
- `.obsidian/templates.json` points to `templates`.
- `AGENTS.md`, `index.md`, and `log.md` exist.
- Example wiki pages exist.
- Obsidian plugin enablement is documented or detected.
- Git is initialized if requested.
- Remote `origin` exists if GitHub backup was requested.
- `main` tracks `origin/main` after push.
- `git status --short` is clean after the first push.

Useful verification commands:

```bash
find <vault-path> -maxdepth 3 -type f
sed -n '1,120p' <vault-path>/.obsidian/templates.json
git -C <vault-path> status --branch --short
git -C <vault-path> remote -v
```

## Human Follow-Up

After the AI finishes, the human should:

- Open the vault in Obsidian.
- Open `LLM-Wiki 入口.md`.
- Install or verify the recommended plugins.
- Configure browser Web Clipper to save articles into `raw/articles/`.
- Configure Obsidian Git:
  - Pull on startup: enabled.
  - Push on backup: enabled if remote exists.
  - Auto backup interval: 10 or 30 minutes.
  - Commit message: `vault backup: {{date}}`.
- Add 5 to 10 source documents for the first topic.
- Ask an AI agent to run `prompts/ingest-source.md` on one source.
- Review the generated wiki pages manually.

## Common Failure Modes

### Wrong Vault Root

Symptom:

```text
The vault path contains wiki/wiki or another duplicated nested root.
```

Fix:

- Move `.obsidian/` and top-level files to the intended vault root.
- Verify the vault root contains `.obsidian/`, `raw/`, `wiki/`, and `LLM-Wiki 入口.md`.

### Obsidian Git Installed But Git Not Initialized

Symptom:

```text
Obsidian Git plugin exists, but git status says "not a git repository".
```

Fix:

```bash
git -C <vault-path> init
```

Then add `.gitignore`, commit, add remote, and push.

### GitHobs Confused With Obsidian Git

Symptom:

```text
Plugin ID is githobs, not obsidian-git.
```

Fix:

- Install `Obsidian Git`.
- Keep or remove `GitHobs` depending on whether GitHub issue editing is needed.

### Web Clipper Not Visible In Vault Files

Symptom:

```text
The human installed the browser extension, but the vault does not show a plugin folder for it.
```

Fix:

- Treat browser Web Clipper as browser-side configuration.
- Verify by clipping a test article into `raw/articles/`.

### Templates Plugin Enabled But Template Folder Not Set

Symptom:

```text
Templates plugin exists, but templates are not found in Obsidian.
```

Fix:

Create or update:

```text
.obsidian/templates.json
```

Set `folder` to `templates`.

## Example Prompt To Execute This SOP

```text
Please execute the SOP "Build an Obsidian LLM-Wiki Based on Karpathy's LLM Wiki Idea".

Target vault path:
/Users/caijinhai/Documents/obsidian/wiki

GitHub repository:
caijinhai/wiki

Repository visibility:
private

Requirements:
- Create the LLM-Wiki structure.
- Add templates, prompts, docs, and AGENTS.md.
- Configure Obsidian Templates.
- Verify Dataview, Omnisearch, Web Clipper, and Obsidian Git.
- Initialize git and push the first commit.
- Do not delete existing notes.
```

## Completion Criteria

This SOP is complete when:

- The vault opens in Obsidian.
- The entry file explains the workflow.
- A source can be added to `raw/articles/`.
- An AI agent can use `AGENTS.md` and `prompts/ingest-source.md` to update the wiki.
- Dataview dashboards can render after plugin installation.
- Git backup works or the remaining Git setup is explicitly documented.

