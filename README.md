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

## Bootstrap a New Project

### 1. Create the Repository

**Option A (GitHub Web - Recommended):**
Click the **Use this template** button on the [BeyondMagic/swe-template](https://github.com/BeyondMagic/swe-template) repository page and select **Create a new repository**. This generates a fresh repository without inheriting upstream template commit history.

**Option B (GitHub CLI):**
```sh
gh repo create <project-name> --template BeyondMagic/swe-template --public --clone
cd <project-name>
```

**Option C (Git Clone Fallback):**
```sh
git clone --depth=1 https://github.com/BeyondMagic/swe-template.git <project-name>
cd <project-name>
rm -rf .git && git init
```

### 2. Run the Initial `/grill-me` Prompt

Open the repository in your coding assistant environment and submit the initial prompt:

```text
/grill-me I am starting a new project using this template.

Project description:
<Describe your project idea in 2-3 sentences: system type, target users, and key architectural goals.>

Walk through the Decision Records sequentially (001-idea through 012-ci-cd-and-tooling). Grill me on each record, propose viable alternatives with clear trade-offs, document our decisions, and mark inapplicable records as Rejected.
```

#### Copy-Paste Examples

**For a Headless Engine or Backend Library (e.g., Database Engine):**
```text
/grill-me I am starting a new project: a high-performance database engine built from zero. It introduces a novel information organization paradigm based on nodes, relationships, and layers with a single source of truth.

Let's go through the Decision Records sequentially. We need technical rigor on 001-idea, 005-quality-factors (throughput, memory safety, predictability), 006-requirements, 007-architecture, 011-testing, and 012-ci-cd. Records 009 (Visual Identity) and 010 (UX Paradigm) do not apply to this headless engine, so we will mark them as Rejected. Grill me record by record.
```

**For a User Interface or Desktop Platform (e.g., Widget & Shell Platform):**
```text
/grill-me I am starting a new project: a modular Widget Interface & Shell Platform. It manages system overlays, desktop panels, and user-facing widgets.

Let's walk through the Decision Records sequentially. We need to establish 001-idea, 007-architecture, 009-visual-identity (colors, typography, icon lockups), 010-ux-paradigm (evaluating intuitive platform conventions vs. keyboard-first power-user ergonomics), and map our core shell flows into Feature Records. Grill me record by record.
```

### 3. Verify Local Documentation

```sh
cd documentation
zensical serve          # Live preview on http://localhost:8000
zensical build --clean  # Static build (must pass with 0 warnings)
```

## Checking Template Updates

Consumer projects can check whether the template scaffolding is current:

1. Inspect the installed version in `.template.json`.
2. Compare with upstream releases:
   ```sh
   git ls-remote --tags https://github.com/BeyondMagic/swe-template
   ```
3. Review [`CHANGELOG.md`](./CHANGELOG.md) and apply scaffolding updates according to the protocol in [`AGENTS.md`](./AGENTS.md).
