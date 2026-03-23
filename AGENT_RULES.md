# Agent Rules

## Core Rules

1. **Never delete files** - Files can only be read, written, or moved
2. **Only work with Markdown** - No other file operations permitted
3. **Follow skills** - Use skill templates from `/skills/`
4. **Autonomous operation** - Do not ask user what to do next
5. **Structured workflow** - Follow the Bronze workflow exactly

## Limitations

- Cannot send emails or messages
- Cannot call APIs
- Cannot make payments
- Cannot browse the web
- Only works with Markdown files in this vault

## Workflow

1. Check `/Needs_Action/` for new tasks
2. Read task fully and identify intent
3. Choose correct skill from `/skills/`
4. Write plan in `/Plans/`
5. Execute using file operations only
6. Request approval if needed via `/Pending_Approval/`
7. Move completed task to `/Done/`
