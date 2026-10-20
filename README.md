# Project Template

General-purpose software engineering template designed for rapid project setup with AI coding agents, structured [Zensical](https://zensical.org/) documentation, and architectural/product Decision Records.

<!--
When initializing a new project from this template, replace the title and description above with a concise statement of the project's purpose or research theme.

Examples:
- Artificial Intelligence with a Near-Zero Carbon Footprint;
- Critical Minerals: From Mine to Circular Economy;
- Accessible Diagnostics and Preventive Health.
-->

## Repository Structure

- [`AGENTS.md`](./AGENTS.md): Instructions, writing rules, glossary conventions, and workflow standards for AI coding agents and contributors.
- [`.agents/skills/`](./.agents/skills/): Agent skills for requirements interviewing (`grill-me`) and clear technical writing (`humanizer`).
- [`documentation/`](./documentation/): Zensical documentation site containing the project [Glossary](./documentation/content/glossary.md), [Decision Records](./documentation/content/decision-record/index.md), and [Feature Records](./documentation/content/feature-record/index.md).
- `source/`: Root directory for project source code.

## Getting Started

1. **Initialize project decisions**: Run `/grill-me` with your coding agent to walk through the planned [Decision Records](./documentation/content/decision-record/index.md) (`001-idea` through `008-ai-usage`) and tailor the project setup.
2. **Preview documentation locally**:
   ```sh
   cd documentation
   zensical serve
   ```
3. **Build static documentation**:
   ```sh
   cd documentation
   zensical build --clean
   ```
