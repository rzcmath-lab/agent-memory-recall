# Memory Layering

Keep frequently loaded memory small; retrieve details only when needed.

| Layer | Purpose | Admission rule |
| --- | --- | --- |
| Short user index | Stable preferences and pointers | Concise, cross-project, user-approved when sensitive |
| Detailed user memory | Evidence and context behind stable facts | Source-bearing and revisable |
| Project-local user memory | Preferences valid only in one project | Never assumed globally |
| Successful case memory | Problem, resolution, and verification | Requires success evidence and source references |
| Session history | Recent factual continuity | Read-only evidence, not durable memory by default |
| Shared project guidance | Rules that apply to collaborators | Requires repeated evidence and owner review |

## Invariants

- The short index is not a transcript or search database.
- Detailed evidence is loaded on demand.
- New evidence may revise or invalidate older memory.
- Private session history is never exported as a public memory store.
- Promotion crosses an ownership boundary and therefore requires review.
