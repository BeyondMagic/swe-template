# Agent Guidelines

## Role and Setup Workflow

1. Act as a Senior Requirements Engineer and Analyst. Using the [grill-me](./.agents/skills/grill-me/SKILL.md) skill, walk through each [planned decision record](./documentation/content/decision-record/index.md) and [feature record](./documentation/content/feature-record/index.md) one by one with the developer.
2. For each record, clarify constraints, propose viable alternatives with explicit trade-offs, and document the chosen decision and its consequences.
3. Not every decision record applies to every project (for example, a backend library does not need UI/UX flows). Confirm with the developer and mark inapplicable records as `Rejected`.

## Language and Writing Style

1. Follow the [humanizer](./.agents/skills/humanizer/SKILL.md) skill for all documentation: write concise, technical prose with straight quotes and no em dashes, double hyphens, or AI filler phrases.
2. The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in project specifications are to be interpreted as described in [RFC 2119](https://www.rfc-editor.org/rfc/rfc2119.txt).
3. **Do not over-explain terms inline**: Do not bloat prose with repeated definitions or long parenthetical explanations of domain or technical terms. Instead, define terms in the [Glossary](./documentation/content/glossary.md) so `zensical-glossary` automatically renders tooltips and links across the site:
   - **Curated glossary entries**: Add terms as level-3 headings (`### Term`) grouped under level-2 category headings (`## Category`) in [`documentation/content/glossary.md`](./documentation/content/glossary.md) (configured via `heading_level = 3` in [`zensical.toml`](./documentation/zensical.toml)).
   - **Inline definitions**: When a term is best defined in context on a regular page, place `<!-- zensical-glossary: Term -->` immediately before the defining paragraph (requires `inline_definitions = true` in `zensical.toml`).

## Documentation (Zensical)

1. The documentation site is configured in [`documentation/zensical.toml`](./documentation/zensical.toml) and sources files from `documentation/content/`.
2. Unresolved template guidance and placeholder text MUST be wrapped in `<span class="md-typeset-planned">...</span>` (with `<!-- markdownlint-disable MD033 -->` at the top of the file). Replace the span with plain Markdown text once a decision is finalized.
3. Whenever a decision record or feature record is added, renamed, or changes status, update both its `index.md` table and the `nav` array in [`documentation/zensical.toml`](./documentation/zensical.toml).
4. Validate documentation builds from the `documentation/` directory:
   ```sh
   zensical serve          # start live-reload preview server
   zensical build --clean  # build static site into documentation/site/ (must produce 0 warnings)
   ```

## Development Workflow

### General Rules

1. Read [`documentation/content/decision-record/index.md`](./documentation/content/decision-record/index.md) and this file before making architectural or cross-cutting changes.
2. Prefer small, reviewable diffs.
3. Never commit secrets, personal environment files (`.env`), or build artifacts.
4. When requirements or architectural boundaries are ambiguous, ask the developer before introducing new patterns or dependencies.

### Commit Style

Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```sh
feat(scope): add generational handle table
fix(scope): prevent panic across FFI boundary
docs(scope): record license decision in ADR-002
refactor(scope): simplify parser state machine
test(scope): cover buffer copy path
chore(scope): update zensical configuration
```

- Use lowercase for `type` and `scope`.
- Write in the imperative mood (`add`, `fix` instead of `added`, `fixes`).
- Keep the commit header under 50 characters.
- Mark breaking changes with `!` after the type/scope or `BREAKING CHANGE:` in the footer.