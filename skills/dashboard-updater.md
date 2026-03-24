# Skill: Dashboard Updater

## Purpose
Keep /Dashboard.md up-to-date with task progress.

## When to Use
- After completing a task
- After creating a new plan
- When approvals are pending
- Periodically to refresh status

## Steps
1. Scan /Plans/ and /Done/ folders
2. Update progress summaries
3. Log completed tasks in /Done/
4. Highlight pending approvals

## Rules
- Do not change original task files
- Only summarize and update Dashboard.md
- Never delete or modify /Plans/ content

## Instructions

1. **Scan folders**
   - Check /Needs_Action/ for pending tasks
   - Check /Plans/ for active plans
   - Check /In_Progress/ for current work
   - Check /Pending_Approval/ for awaiting human
   - Check /Done/ for completed tasks

2. **Count and categorize**
   - Total tasks by status
   - Recent completions
   - Upcoming deadlines (if noted)

3. **Update Dashboard.md**
   - Refresh all counts
   - Update task lists
   - Highlight urgent items
   - Note pending approvals

4. **Preserve history**
   - Keep recent completed tasks visible
   - Archive older items to summary counts

## Output Format

Update `/Dashboard.md` with this structure:

```markdown
# Dashboard

**Last Updated**: [timestamp]

## Quick Stats

| Status | Count |
|--------|-------|
| Pending | X |
| In Progress | X |
| Awaiting Approval | X |
| Completed Today | X |

## ⚠️ Needs Attention

### Pending Approvals
- [ ] [Task name] - [waiting since]

### Urgent Tasks
- [ ] [Task name] - [reason]

## 📋 Active Tasks

### In Progress
- [Task name] - [status]

### Planned
- [Task name] - [plan link]

## ✅ Recently Completed

- [Task name] - [completed date]
- [Task name] - [completed date]

## 📁 Folder Status

- /Needs_Action/: X files
- /Plans/: X files
- /In_Progress/: X files
- /Pending_Approval/: X files
- /Done/: X files
```

## Example

**Trigger**: Task moved to /Done/

**Action**:
1. Scan all folders
2. Update counts in Dashboard.md
3. Add completed task to "Recently Completed"
4. Remove from "In Progress"
