# Logging Policy

All agent actions must be logged for accountability and debugging.

## Log Format

Each log entry should include:

```
## [Timestamp] - [Action Type]

**Task**: [Task name or ID]
**Action**: [What was done]
**Result**: [Success/Failure + details]
**Files Affected**: [List of files read/written/moved]
```

## What to Log

- Task pickup from `/Needs_Action/`
- Plan creation
- Each execution step
- Approval requests
- Task completion
- Errors or failures

## Log File Naming

`YYYY-MM-DD_task-name.md`

Example: `2024-01-15_write-summary.md`

## Retention

Logs are kept indefinitely in `/Logs/` for audit purposes.
