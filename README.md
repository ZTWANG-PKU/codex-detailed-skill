# Detailed: a Codex skill for deep scientific-paper reading

`Detailed` is a Chinese-language Codex skill for source-gated, figure-by-figure reading of scientific papers. It reviews the main text, supplementary materials, Extended/Source Data, public datasets, and the official code repository when available.

The workflow is designed to avoid a common failure mode in paper summaries: producing a confident “deep read” from an abstract, preview page, or incomplete source. If a readable full text is unavailable, the skill reports the missing source and asks the user to provide the paper before continuing.

## What it does

- Verifies paper identity, version, DOI/PMID/PMCID/preprint links, and correction or retraction status.
- Requires a readable full text before beginning a detailed review.
- Builds a material inventory covering the paper, supplements, Extended/Source Data, datasets, protocols, and official code.
- Visually inspects every main figure and explains every discernible panel.
- Reconstructs the evidence chain from figure to caption, Results, Methods, supplements, source data, and code.
- Reviews study design, statistics, leakage risks, external validation, reproducibility, and alternative explanations.
- Produces a Chinese report with scientific takeaways, transferable methods, and testable research ideas.
- Ends with verified legal full-text and resource links.

## Install in Codex

The easiest method is to invoke Codex's built-in skill installer and provide this repository path:

```text
$skill-installer https://github.com/ZTWANG-PKU/codex-detailed-skill/tree/main/skills/detailed
```

You can also ask Codex in natural language:

```text
Use $skill-installer to install the Detailed skill from
https://github.com/ZTWANG-PKU/codex-detailed-skill/tree/main/skills/detailed
```

After installation, Codex normally detects the skill automatically. If it does not appear, restart Codex. Current OpenAI documentation also describes user skills under `$HOME/.agents/skills` and repository skills under `.agents/skills`.

## Use

Explicit invocation:

```text
$detailed 精读这篇论文：https://doi.org/...
```

With a local PDF:

```text
$detailed 精读 /absolute/path/to/paper.pdf，并检查补充材料和官方代码。
```

Codex may also select the skill automatically for requests that clearly ask for a full-paper, figure-by-figure review.

## Repository layout

```text
.
├── .codex-plugin/plugin.json
└── skills/detailed/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
        ├── acquisition-protocol.md
        ├── figure-protocol.md
        └── report-spec.md
```

The plugin manifest makes the repository ready to be distributed as a Codex plugin as well as a standalone skill. The direct skill-installer workflow above is the simplest way to use the GitHub version locally.

## Portability and permissions

This public version contains no personal server paths or credentials. Reports are saved only when the user asks for a file or the active task requires an artifact, and the destination must be inside an authorized workspace or explicitly supplied by the user. Uploads, remote writes, large downloads, and execution of third-party code remain subject to the current Codex environment's permissions and user authorization.

## License

MIT License. See [LICENSE](LICENSE).

## Security note

Skills are instructions that can influence an agent's tool use. Review any third-party skill before installing it, especially when network access, external writes, or executable scripts are involved.
