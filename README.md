# Bronze Tier Digital FTE Vault

This is an Obsidian-style vault for a Bronze Tier AI employee.

## Purpose

The Bronze tier is the simplest level of autonomy. The agent:
- Works ONLY with Markdown files
- Cannot send emails, call APIs, make payments, or browse the web
- Reads, writes, and moves files within this vault

## Folder Structure

| Folder | Purpose |
|--------|---------|
| `/Needs_Action/` | Incoming tasks to be processed |
| `/Plans/` | Step-by-step execution plans |
| `/Pending_Approval/` | Tasks awaiting human approval |
| `/In_Progress/` | Tasks currently being executed |
| `/Done/` | Completed tasks |
| `/Logs/` | Task execution logs |
| `/skills/` | Skill references for task types |

## How to Use

1. Drop a Markdown file into `/Needs_Action/`
2. The agent will read it, create a plan, and execute
3. Check `/Pending_Approval/` if human input is needed
4. Find completed work in `/Done/`
