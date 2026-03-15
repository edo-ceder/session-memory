Re-summarize the current session from scratch and re-inject the fresh memory.

Use this when Claude is drifting, contradicting earlier decisions, or before a major code change.

## Steps

1. Run the refresh script — it automatically detects the current session and extracts memory:
```bash
~/.claude/hooks/session-memory/refresh.sh
```

2. The script outputs the session ID and memory file path. Read the memory file it produced.

3. Give the user a brief summary (2-3 sentences) of the session goal and current state, confirming you're back on track. Mention any active blockers or recent corrections.

$ARGUMENTS
