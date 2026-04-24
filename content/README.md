# Welcome to Quartz

This is your digital garden built with Quartz.

## Getting Started

1. Add markdown files to the `content` folder
2. Run `npx quartz build` to build the site
3. Run `npx quartz serve` to preview locally

## Memory Structure

```
content/
├── Memory/
│   ├── Private/    # Private notes (not published)
│   └── Public/     # Public notes (published to git)
```

## Notes

- Files in `Private` folder can be excluded from publishing
- Use frontmatter to control visibility
- Quartz supports Obsidian-flavored markdown