# Setup Files Manifest

*Read this fresh each time Narrated Setup duplicates files locally — not from memory. Source files live at `https://projectgrommet.com/setup-files/<name>`.*

| Source | Local destination | Kind | Behaviour |
|---|---|---|---|
| CLAUDE_template.md | CLAUDE.md | Template | Duplicated once, renamed, then owned and edited by the project |
| project-context-template.md | project-context.md | Template | Duplicated once, renamed, then grows with the project |
| boal-check.md | boal-check.md | Reference | Duplicated once, read repeatedly via tool call, never edited by the project |
| boal-check-log.md | boal-check-log.md | Template | Duplicated once (blank), then appended to |

| continuity-check.md | continuity-check.md | Reference | Duplicated once, read repeatedly via tool call, never edited by the project |
| continuity-check-log.md | continuity-check-log.md | Template | Duplicated once (blank), then appended to |
| needs-based-communication.md | needs-based-communication.md | Reference | Duplicated once, read repeatedly, never edited by the project |
| enneagram-map.md | enneagram-map.md | Reference | Duplicated once, read repeatedly, never edited by the project |

| Tracker.md | Tracker.md | Template | Duplicated once, then edited directly |

**Reference** files are never modified locally — if the source changes, re-fetch it.
**Template** files are duplicated once and then belong to the project; the source copy is never re-fetched over them.
