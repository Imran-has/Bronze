# Skill: WhatsApp Triage

## Purpose
Analyze WhatsApp messages and decide next action.

## When to Use
- Task contains WhatsApp message content to be triaged
- Task mentions "WhatsApp", "message", "chat"
- Need to prioritize or respond to messaging communications

## Steps
1. Read message content
2. Detect keywords (urgent, invoice, payment, help)
3. Decide priority
4. Create plan in /Plans/
5. Request human approval for any external action

## Rules
- Never send messages
- Only create plans
- Only work with files in the vault

## Instructions

1. **Read message content**
   - Who sent the message?
   - What is the context (individual chat, group)?
   - When was it sent?

2. **Detect keywords**
   - **Urgent indicators**: urgent, ASAP, emergency, help, now
   - **Financial**: invoice, payment, money, transfer, price
   - **Questions**: ?, how, what, when, where, why
   - **Requests**: please, can you, need, want

3. **Decide priority**
   - **High**: Contains urgent keywords, financial matters, time-sensitive
   - **Medium**: Questions requiring response, general requests
   - **Low**: FYI messages, social messages, can wait

4. **Determine action**
   - Reply needed?
   - Task to create?
   - Information to note?
   - No action required?

5. **Create output**
   - Triage summary document
   - Plan in /Plans/ if action needed
   - Approval request if reply is needed

## Output Format

```markdown
# WhatsApp Triage: [Sender/Group Name]

**From**: [sender]
**Date**: [date]
**Priority**: High / Medium / Low

## Keywords Detected
- [keyword 1]
- [keyword 2]

## Message Summary
[Brief summary of message content]

## Intent
[What the sender wants]

## Recommended Action
- [ ] Reply needed
- [ ] Create task
- [ ] Note information
- [ ] No action

## Next Steps
[Specific actions to take]

## Draft Reply (if applicable)
> [Draft text - REQUIRES HUMAN APPROVAL]
```

## Example

**Task**: WhatsApp message "Hi, can you send the invoice urgently? Need it for payment today"

**Output**:
- Triage document showing High priority
- Keywords: urgent, invoice, payment
- Plan created in /Plans/
- Approval request in /Pending_Approval/ with draft reply
