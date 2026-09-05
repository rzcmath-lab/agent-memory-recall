# Recall Policy

## Trigger signals

Recall is useful when the user references prior discussion, a previously supplied file, an established convention, an earlier decision, or a repeated failure while the current context lacks sufficient evidence.

## Search order

1. Normalize the current question into a few concrete terms.
2. Search a lightweight recent-history index.
3. Inspect no more evidence than needed to resolve the immediate gap.
4. If the question is clearly older and recent history misses, search verified cases once.
5. Ask the user when evidence remains ambiguous or contradictory.

## Grep-first pattern

The following command illustrates lexical retrieval against synthetic, redacted records:

```bash
rg -n -i 'previous decision|retry failure|expected output' ./synthetic-history-index/
```

Real paths, identifiers, and records must not appear in public documentation.

## Stop conditions

Stop searching when a top source contains the topic and decision needed to answer. Continue only when the user asks for the complete artifact, the hit contains only a title or identifier, or the evidence describes failure without an actual conclusion.

Do not expand into unlimited history for completeness alone.
