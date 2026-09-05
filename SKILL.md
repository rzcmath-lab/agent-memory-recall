---
name: agent-memory-recall
description: Recover missing context from recent history or verified case memory when a user references prior work, established preferences, or a repeated failure. Use for evidence-first recall and durable-memory maintenance; do not use it to debug product code or silently create shared project rules.
---

# Agent Memory Recall

Use memory to restore evidence, not to manufacture certainty.

## Route the request

Choose one outcome:

- `context_recall`: recover facts from recent history.
- `durable_memory_candidate`: propose a stable user preference or fact.
- `case_memory_candidate`: record a verified successful resolution.
- `promotion_candidate`: propose that a repeatedly verified pattern belongs in shared project guidance.
- `reject`: evidence is insufficient, sensitive, contradictory, or outside scope.

## Recall workflow

1. Identify the missing context: subject, decision, file, failure signature, tool, or expected output.
2. Search a redacted recent-history index first. Prefer deterministic lexical search before semantic expansion.
3. Inspect only the top bounded evidence windows and retain their source references.
4. Stop when one window contains enough evidence to answer the user's immediate question.
5. If recent history does not answer a non-recent question, search verified case memory once.
6. State whether the answer comes from recent history, durable memory, or a past successful case.
7. Treat every hit as temporary evidence unless it passes the relevant write criteria.

Do not enumerate unrelated storage directories, scan unlimited history, or expose raw records merely to make an answer feel more complete.

## Evidence requirements

A recalled item should include:

- a stable, non-sensitive source reference;
- the observed problem or decision;
- the relevant resolution or conclusion;
- success evidence when it is presented as a successful case;
- uncertainty when evidence is incomplete or conflicting.

Without success evidence, a prior attempt is weak context—not a reusable solution.

## Writing durable memory

Only propose durable memory when the information is stable across projects or clearly represents a lasting user preference. Require user confirmation before saving sensitive data or any memory that changes future behavior.

Do not store one-off requests, full transcripts, credentials, private identifiers, confidential business rules, or unsupported inferences.

## Promoting shared guidance

A successful case does not automatically become a project rule. Promotion requires repeated evidence, applicability beyond one incident, and an owner review. This skill may produce a promotion candidate but must not edit shared guidance itself.

## Privacy

Apply [the public and operational privacy boundary](./references/privacy-boundary.md) before displaying, saving, or exporting memory-derived material. Read [memory layering](./references/memory-layering.md) when deciding where an item belongs, and [recall policy](./references/recall-policy.md) for search order and stopping conditions.
