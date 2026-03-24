# Skill: Email Triage

## Purpose
Analyze incoming emails and decide the next action.

## When to Use
- Task contains email content to be triaged
- Task mentions "email", "inbox", "message triage"
- Need to prioritize or categorize communications

## Steps
1. Identify sender
2. Detect intent
3. Decide priority
4. Create plan
5. Request human approval if reply is needed

## Rules
- Never send emails directly
- Always create approval in /Pending_Approval/ before drafting any reply
- Only work with files; do not access email servers or APIs

## Instructions

1. **Identify sender**
   - Who sent the email?
   - What is their relationship (client, colleague, vendor, unknown)?

2. **Detect intent**
   - What does the sender want?
   - Is it a request, information, question, or FYI?

3. **Decide priority**
   - **High**: Urgent, time-sensitive, from important contacts
   - **Medium**: Requires action but not urgent
   - **Low**: FYI, newsletters, can wait

4. **Determine action**
   - Reply needed?
   - Forward to someone?
   - Archive/file?
   - Follow-up task?

5. **Create output**
   - Triage summary document
   - If reply needed: create approval request first

## Output Format

```markdown
# Email Triage: [Subject Line]

**From**: [sender]
**Date received**: [date]
**Priority**: High / Medium / Low

## Intent
[What the sender wants]

## Recommended Action
- [ ] Reply needed
- [ ] Forward to: [person]
- [ ] Create task
- [ ] Archive

## Next Steps
[Specific actions to take]

## Draft Reply (if applicable)
> [Draft text - REQUIRES APPROVAL]
```

## Example

**Task**: Email from client asking about project timeline

**Output**:
- Triage document showing High priority
- Approval request in /Pending_Approval/ with draft reply
- Human reviews and approves before any response is prepared
