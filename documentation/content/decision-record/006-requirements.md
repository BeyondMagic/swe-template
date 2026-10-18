---
icon: lucide/list-checks
---

<!-- markdownlint-disable MD033 -->

# 006: Requirements

- **Type:** Product
- **Status:** <span class="md-typeset-planned">Planned</span>
- **Date:** <span class="md-typeset-planned">YYYY-MM-DD</span>
- **Author(s) / Deciders:** <span class="md-typeset-planned">Project authors and requirements analysts</span>
- **Question:** What functional and non-functional requirements MUST the system satisfy, and how are they traced to features?

## Context

<span class="md-typeset-planned">Establish the baseline functional capabilities, system constraints, and acceptance criteria before detailed implementation begins. Individual feature workflows should be broken out into dedicated [Feature Records](../feature-record/index.md).</span>

## Requirements and Restrictions

### Functional Requirements

- <span class="md-typeset-planned">**FR-01:** The system MUST ...</span>
- <span class="md-typeset-planned">**FR-02:** The system SHOULD ...</span>

### Non-Functional Requirements

- <span class="md-typeset-planned">**NFR-01 (Performance):** Target throughput, startup time, or memory budget.</span>
- <span class="md-typeset-planned">**NFR-02 (Security & Privacy):** Data handling, authentication, or sandboxing constraints.</span>
- <span class="md-typeset-planned">**NFR-03 (Portability):** Supported operating systems, architectures, and runtime versions.</span>

## Alternatives

- <span class="md-typeset-planned">**Informal Issue Tracking Only:** Tracking requirements solely in ad-hoc issue tickets makes system-wide constraints and [RFC 2119](../glossary.md) invariants hard to audit.</span>

## Decision

<span class="md-typeset-planned">Document system-level functional and non-functional requirements here using RFC 2119 keywords, and link user-facing workflows to their corresponding [Feature Records](../feature-record/index.md).</span>

## Consequences

### Positives

- <span class="md-typeset-planned">Clear traceability between high-level project scope ([001: Idea](./001-idea.md)), quality priorities ([005: Quality Factors](./005-quality-factors.md)), and individual features.</span>

### Negatives

- <span class="md-typeset-planned">Requires keeping this record updated when core system invariants change.</span>

