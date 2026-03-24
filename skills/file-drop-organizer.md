# Skill: File Drop Organizer

## Purpose
Handle newly dropped files in /Inbox or /Needs_Action/.

## When to Use
- New files appear in /Inbox/ or /Needs_Action/
- Files need categorization and organization
- Task mentions "organize", "sort", "categorize" incoming files

## Steps
1. Detect new files
2. Categorize by type (invoice, report, document)
3. Move to /Needs_Action/
4. Create metadata file with details
5. Create a plan in /Plans/ if action is required

## Rules
- Do not delete files
- Only organize and create metadata

## Instructions

1. **Detect new files**
   - Check /Inbox/ and /Needs_Action/ for files
   - Note filename, date modified
   - Read file contents

2. **Categorize by type**
   - **Invoice**: Contains payment terms, amounts, due dates
   - **Report**: Analysis, summaries, data presentations
   - **Document**: General documents, letters, memos
   - **Notes**: Meeting notes, personal notes
   - **Request**: Action items, asks, tasks
   - **Reference**: Information for future use

3. **Create metadata file**
   - Document key details about the file
   - Tag with category
   - Note any actions required

4. **Determine if action needed**
   - Does file require response?
   - Does file have a deadline?
   - Is follow-up needed?

5. **Create plan if needed**
   - If action required, create plan in /Plans/
   - Reference the original file

## Output Format

### Metadata File
```markdown
# Metadata: [Original Filename]

**Original file**: [filename]
**Detected**: [date]
**Category**: Invoice / Report / Document / Notes / Request / Reference

## Details
- **Type**: [specific type]
- **From**: [source if known]
- **Date**: [document date]
- **Subject**: [brief subject]

## Tags
- [tag1]
- [tag2]

## Action Required
- [ ] Yes - [description]
- [ ] No

## Related Files
- [any related files]

## Notes
[Additional observations]
```

### Folder Structure
```
/Needs_Action/
  - original-file.md
  - original-file_metadata.md
/Plans/
  - plan-for-original-file.md (if action needed)
```

## Example

**Task**: New file "Q4-sales-report.md" dropped in /Inbox/

**Output**:
- Metadata file: `Q4-sales-report_metadata.md`
  - Category: Report
  - Tags: sales, Q4, quarterly
  - Action: Review and summarize
- Plan created: `plan-Q4-sales-report.md` in /Plans/
