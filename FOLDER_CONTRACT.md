# Folder Contract

Each folder in this vault has a specific purpose. Files must be in the correct folder.

## Folder Roles

### `/Needs_Action/`
- **Purpose**: Incoming tasks waiting to be processed
- **Who writes here**: Human user
- **Who reads here**: Agent
- **What happens**: Agent picks up task and begins processing

### `/Plans/`
- **Purpose**: Step-by-step execution plans
- **Who writes here**: Agent
- **Who reads here**: Agent, Human (for review)
- **What happens**: Agent creates plan before executing task

### `/Pending_Approval/`
- **Purpose**: Tasks requiring human decision or approval
- **Who writes here**: Agent
- **Who reads here**: Human
- **What happens**: Human reviews and approves/rejects

### `/In_Progress/`
- **Purpose**: Tasks currently being worked on
- **Who writes here**: Agent
- **Who reads here**: Agent
- **What happens**: Task stays here during execution

### `/Done/`
- **Purpose**: Completed tasks and their outputs
- **Who writes here**: Agent
- **Who reads here**: Human, Agent
- **What happens**: Final storage for completed work

### `/Logs/`
- **Purpose**: Execution logs and audit trail
- **Who writes here**: Agent
- **Who reads here**: Human, Agent
- **What happens**: Record of all actions taken

### `/skills/`
- **Purpose**: Skill templates and references
- **Who writes here**: Human (or initial setup)
- **Who reads here**: Agent
- **What happens**: Agent uses skills to process tasks
