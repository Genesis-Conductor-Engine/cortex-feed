## Yennefer Cortex Feed

**Live JSONL source of truth** for the [Yennefer Cortex Dashboard](https://github.com/Genesis-Conductor-Engine/yennefer-cortex).

### Consumption

The dashboard polls:

```
https://raw.githubusercontent.com/Genesis-Conductor-Engine/cortex-feed/main/feed.jsonl
```

### Schema (per line)

```json
{
  "event_id": "cortex-YYYYMMDD-XXX",
  "timestamp": "ISO8601",
  "type": "cortex_state_snapshot" | "inversion" | "maru_reframe",
  "epsilon_th": 0.0-1.0,
  "crystalline_score": 0.0-1.0,
  "dissonance_r": 0.0-1.0,
  "content": { ... },
  "source": "daemon" | "github" | "manual",
  "trace_consent_id": "...",
  "orcid_attribution": "0009-0008-8389-1297"
}
```

### Adding Events

Append new JSON objects as single lines to `feed.jsonl`.

This feed powers the live thermodynamic metrics surface for Genesis Conductor.
