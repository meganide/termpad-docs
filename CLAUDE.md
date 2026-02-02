# Mintlify documentation

## Working relationship
- You can push back on ideas-this can lead to better documentation. Cite sources and explain your reasoning when you do so
- ALWAYS ask for clarification rather than making assumptions
- NEVER lie, guess, or make up information

## Project context
- Format: MDX files with YAML frontmatter
- Config: docs.json for navigation, theme, settings
- Components: Mintlify components

## Content strategy
- Document just enough for user success - not too much, not too little
- Prioritize accuracy and usability of information
- Make content evergreen when possible
- Search for existing information before adding new content. Avoid duplication unless it is done for a strategic reason
- Check existing patterns for consistency
- Start by making the smallest reasonable changes

## Frontmatter requirements for pages
- title: Clear, descriptive page title
- description: Concise summary for SEO/navigation

## Writing standards
- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Include both basic and advanced use cases
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links

## Git workflow
- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development
- NEVER skip or disable pre-commit hooks

## Changelogs
- Use `<Update>` components for all changelog entries
- Each Update must have `label` (date) and `description` (version) properties
- Include `rss: true` in changelog frontmatter for RSS feed support
- Add `tags` array to Updates for filtering capability (e.g., tags={["Features", "Bug Fixes"]})
- RSS feed publishes at page URL + /rss.xml
- Each Update label creates table of contents entry automatically
- Updates support markdown, links, images, and demos
- RSS feeds contain pure Markdown only - use `rss` property for alternative text if needed

### Changelog update format
```mdx
<Update label="Month Year" description="vX.X.X" tags={["Category"]}>
  Content goes here with markdown support
</Update>
```

## Do not
- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions - always ask for clarification