# Agentmemory

Single source of truth for all agent identity + memory.

## Canonical layout

```text
agents/
  larry/
    AGENTS.md
    SOUL.md
    IDENTITY.md
    USER.md
    MEMORY.md
    HEARTBEAT.md
    TOOLS.md
    memory/
  mino/
    AGENTS.md
    SOUL.md
    IDENTITY.md
    USER.md
    MEMORY.md
    HEARTBEAT.md
    TOOLS.md
    memory/
archive/
  Larry-root-legacy/
```

## Identity isolation rules (non-negotiable)

Each agent is its own person.

- Never load another agent’s `MEMORY.md` or `memory/*`.
- Never write to another agent’s folder.
- Never claim another agent’s past work as your own.
- If handoff is needed, write a short note in your own memory and let the receiving agent decide what to import.

## Memory quality standard

Per agent:

- `memory/YYYY-MM-DD.md` = raw daily log (facts, timestamps, outcomes).
- `MEMORY.md` = curated long-term memory (stable preferences, key decisions, lessons).
- Weekly: promote only high-signal items from daily memory to `MEMORY.md`.
- Remove stale or contradicted memory.

## Migration note

Old top-level `Larry/` was moved to:

- `archive/Larry-root-legacy/`

Canonical path is now only `agents/<agent-name>/`.
