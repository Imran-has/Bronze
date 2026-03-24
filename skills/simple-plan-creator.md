# Skill: Simple Plan Creator

## Purpose
Create step-by-step plans for any incoming task.

## When to Use
- Any new task arrives in /Needs_Action/
- Task requires multiple steps to complete
- Need to break down a complex request

## Steps
1. Read task file in /Needs_Action/
2. Identify required steps
3. Write steps in /Plans/
4. Tag steps that need human approval
5. Move task forward only via file operations

## Rules
- Do not execute actions outside file system
- Always request human approval for sensitive tasks

## Instructions

1. **Read task file**
   - Open the task file in /Needs_Action/
   - Understand the full request
   - Note any constraints or requirements

2. **Identify required steps**
   - Break task into discrete actions
   - Order steps logically
   - Identify dependencies between steps

3. **Classify each step**
   - **File operation**: Can do autonomously
   - **Requires skill**: Reference the skill needed
   - **Needs approval**: Mark for human review
   - **External action**: Cannot do - flag for human

4. **Write plan**
   - Create plan file in /Plans/
   - List all steps with checkboxes
   - Tag approval-required steps clearly

5. **Identify sensitive tasks**
   Requires human approval:
   - Financial decisions
   - External communications
   - Data sharing
   - Irreversible actions
   - Anything with significant impact

## Output Format

```markdown
# Plan: [Task Name]

**Source**: /Needs_Action/[task-file].md
**Created**: [date]
**Status**: Draft

## Objective
[One sentence goal]

## Steps

1. [ ] Step description
   - **Type**: File operation
   - **Skill**: [skill if applicable]

2. [ ] Step description
   - **Type**: Requires approval ⚠️
   - **Reason**: [why approval needed]

3. [ ] Step description
   - **Type**: External action 🚫
   - **Note**: Human must complete this step

## Approval Required
- [ ] Step 2: [reason]

## Dependencies
- Step 2 depends on Step 1
- Step 3 depends on Step 2

## Expected Output
[What will be produced]

## Notes
[Any additional context]
```

## Approval Tags

Use these markers in plans:
- ✅ Can execute autonomously
- ⚠️ Requires human approval
- 🚫 Cannot execute (external action)

## Example

**Task**: "Send quarterly report to client"

**Plan**:
1. ✅ Locate quarterly report file
2. ✅ Review report for completeness
3. ⚠️ Draft email to client (needs approval)
4. 🚫 Send email (human must do)

**Result**: Plan created with steps 3-4 flagged for human action
