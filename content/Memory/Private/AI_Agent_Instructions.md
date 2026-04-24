---
title: AI Agent Instructions - Memory Management
tags:
  - instructions
  - agent
  - memory
---

# Instructions for AI Agents

This file contains instructions for adding content to the Memory system.

## Quick Reference

### Memory Location
```
C:\repo\quartz\content\Memory\
```

### Two Types of Memory

| Type | Location | Visibility | Use Case |
|------|----------|------------|----------|
| **Private** | `Memory/Private/` | Not published to git | AI context, agent memory, sensitive info |
| **Public** | `Memory/Public/` | Published to git | Blog posts, public docs |

---

## How to Add Content

### When I say: "Add to my private memory"

1. Determine the appropriate folder:
   - **Applications** - Apps, projects, software
   - **Learnings** - Things you learned
   - **Future Ideas** - Project ideas, plans
   - **Concepts** - Technical concepts, tutorials

2. Save to: `C:\repo\quartz\content\Memory\Private\[FOLDER]\filename.md`

3. Use this template:
   ```markdown
   ---
   title: [Title]
   tags:
     - [relevant-tags]
   ---

   # [Title]

   [Content here]
   ```

### When I say: "Add to my public memory"

1. Save to: `C:\repo\quartz\content\Memory\Public\[FOLDER]\filename.md`

2. Same template as above

---

## File Naming Convention

- Use lowercase
- Use hyphens for spaces: `my-new-app.md`
- Be descriptive: `react-native-setup.md` not `rn.md`

---

## Adding to Existing Files

If file exists:
1. Read the current content
2. Append or update relevant section
3. Preserve frontmatter

---

## Folder Structure

```
Memory/
├── Private/
│   ├── Applications/
│   │   ├── EmmanuelMobileApp.md
│   │   ├── AttendanceManagement.md
│   │   └── [app-name].md
│   ├── Learnings/
│   ├── Future Ideas/
│   └── Concepts/
└── Public/
    ├── Applications/
    ├── Learnings/
    ├── Future Ideas/
    └── Concepts/
```

---

## Build & Preview

After adding content:
```bash
cd C:\repo\quartz
npx quartz build
cd public
npx http-server
```

---

## Summary

| User Command | Action |
|------------|--------|
| "Add [X] to my private memory" | Save to `Memory/Private/[folder]/` |
| "Add [X] to my public memory" | Save to `Memory/Public/[folder]/" |
| "Update [file]" | Edit existing file |
| "Create new folder [name]" | Create `Memory/Private/[name]/` |