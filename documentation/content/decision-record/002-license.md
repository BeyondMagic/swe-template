---
icon: lucide/scale
---

<!-- markdownlint-disable MD033 -->

# 002: License Selection

- **Type:** Strategy
- **Status:** <span class="md-typeset-planned">Planned</span>
- **Date:** <span class="md-typeset-planned">YYYY-MM-DD</span>
- **Author(s) / Deciders:** <span class="md-typeset-planned">Repository owners and legal/project stakeholders</span>
- **Question:** Under what license terms will this project's source code, documentation, and assets be distributed?

## Context

<span class="md-typeset-planned">A software project without a license defaults to exclusive copyright, preventing others from legally using, modifying, or redistributing the work. Selecting an explicit license clarifies permissions, patent grants, and attribution requirements.</span>

## Requirements and Restrictions

- <span class="md-typeset-planned">**Commercial & Derivative Use:** Determine whether proprietary derivatives are allowed or if modifications must remain open-source (copyleft).</span>
- <span class="md-typeset-planned">**Patent Protection:** Determine whether an explicit patent grant and retaliation clause are required.</span>
- <span class="md-typeset-planned">**Dependency Compatibility:** Ensure compatibility with the licenses of third-party libraries used by the project.</span>

## Alternatives

- <span class="md-typeset-planned">**MIT / BSD-2-Clause (Permissive):** Minimal restrictions, high adoption, no explicit patent grant clause.</span>
- <span class="md-typeset-planned">**Apache-2.0 (Permissive + Patent Grant):** Permissive use with an explicit patent license and retaliation clause.</span>
- <span class="md-typeset-planned">**MPL-2.0 (Weak Copyleft):** File-level copyleft allowing combination with proprietary files in larger works.</span>
- <span class="md-typeset-planned">**GPL-3.0-or-later / AGPL-3.0-or-later (Strong Copyleft):** Requires derivative works (and network deployments for AGPL) to be distributed under the same license.</span>
- <span class="md-typeset-planned">**Proprietary / All Rights Reserved:** Closed-source distribution restricted to authorized parties.</span>

## Decision

<span class="md-typeset-planned">Specify the chosen SPDX license identifier (for example, `MIT`, `Apache-2.0`, or `GPL-3.0-only`) for code and, if different, for documentation and media assets (such as `CC-BY-4.0`).</span>

## Consequences

### Positives

- <span class="md-typeset-planned">Contributors and downstream users have unambiguous legal terms for adoption and contribution.</span>

### Negatives

- <span class="md-typeset-planned">Changing a license later requires consent from all copyright holders or a Contributor License Agreement (CLA).</span>

