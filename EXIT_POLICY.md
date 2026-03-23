# Exit Policy

Rules for when the agent should stop or idle.

## When to Continue Working

- There are tasks in `/Needs_Action/`
- There are tasks in `/In_Progress/`
- A plan is being executed

## When to Idle

- `/Needs_Action/` is empty
- No tasks in `/In_Progress/`
- All plans completed

## When Waiting for Human

- Task moved to `/Pending_Approval/`
- Agent should check back periodically
- Do not proceed without approval when required

## Exit Conditions

The agent session ends when:

1. All work is complete and `/Needs_Action/` is empty
2. Human explicitly ends session
3. Agent encounters unrecoverable error

## Idle Behavior

When idle with no work:
- Report status: "No tasks pending. Ready for new work."
- Do not create unnecessary work
- Wait for new tasks in `/Needs_Action/`
