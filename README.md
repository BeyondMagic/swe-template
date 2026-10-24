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

- [`.template.json`](./.template.json): Template version manifest tracking upstream repository and managed scaffolding paths.
- [`CHANGELOG.md`](./CHANGELOG.md): History of template releases and additions following Keep a Changelog.
- [`AGENTS.md`](./AGENTS.md): Instructions, writing rules, glossary conventions, and workflow standards for AI coding agents and contributors.
- [`.agents/skills/`](./.agents/skills/): Agent skills for requirements interviewing (`grill-me`) and clear technical writing (`humanizer`).
- [`documentation/`](./documentation/): Zensical documentation site containing the project [Glossary](./documentation/content/glossary.md), [Decision Records](./documentation/content/decision-record/index.md), and [Feature Records](./documentation/content/feature-record/index.md).
- `source/`: Root directory for project source code.
- `tests/`: Root directory for automated unit, integration, and black-box test suites.

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

## Checking Template Updates

Consumer projects can check whether the template scaffolding is current:

1. Inspect the installed version in `.template.json`.
2. Compare with upstream releases:
   ```sh
   git ls-remote --tags https://github.com/BeyondMagic/template
   ```
3. Review [`CHANGELOG.md`](./CHANGELOG.md) and apply scaffolding updates according to the protocol in [`AGENTS.md`](./AGENTS.md).
