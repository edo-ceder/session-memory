Re-summarize the current session from scratch and re-inject the fresh memory.

Use this when Claude is drifting, contradicting earlier decisions, or before a major code change. This extracts a structured snapshot of the session (goals, decisions, state, blockers, corrections) and loads it into your current context.

## Steps

1. Find the current session's transcript file. Look in `~/.claude/projects/` for the JSONL file matching this session. The session ID is in the transcript filename.

2. Run the extraction script, passing the session ID and transcript path:
```bash
~/.claude/hooks/session-memory/extract.sh <session_id> <transcript_path>
```

3. Read the resulting memory file at `~/.claude/session-memories/<session_id>.md`.

4. Internalize the content — these are structured notes from this session. Verify any specific details (file contents, deployment state) by checking the source before acting.

5. Give the user a brief summary (2-3 sentences) of the session goal and current state, confirming you're back on track. Mention any active blockers or recent corrections.

$ARGUMENTS
