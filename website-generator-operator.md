# Website Generator & Operator

**Purpose:** Build new websites from scratch and generate operations manuals for effortless future maintenance.

---

## Workflow

### Phase 1 — Plan Architecture
Before writing a single line of code:
1. Understand the site's purpose (landing page, blog, portfolio, webapp, game, etc.)
2. Determine tech stack (vanilla HTML/CSS/JS preferred unless user specifies otherwise)
3. Plan file structure
4. Plan component tree and data flow
5. Plan deployment target (static hosting, etc.)

### Phase 2 — Build the Site
1. Create the project folder under the user's workspace
2. Build all files with clean, semantic code
3. Ensure mobile responsiveness
4. Ensure dark/light theme support if applicable
5. Add basic SEO meta tags
6. Verify no console errors

### Phase 3 — Generate Operations Manual (CRITICAL)
After building, **automatically create** `[project_name]_operations.md` in `G:\Welcome\.agents\skills\` containing:

#### Operations Manual Template

```markdown
# [Project Name] — Operations Manual

## Quick Start
- Location: `[full path to project folder]`
- Tech Stack: [list]
- Deployment: [how it's deployed]

## Content Updates
### How to add new [videos/posts/items]:
- File to edit: `content/[type]/index.json`
- Required fields: [list fields with examples]
- Example entry:
```json
{
  "id": "example-id",
  "title": "Example Title",
  "description": "Description here",
  ...
}
```

### How to change styling:
- Primary stylesheet: `assets/css/style.css`
- CSS variables for theming: [list key variables]
- Key selectors: [list important classes/IDs]

### How to add a new page:
1. Create `[pagename].html` in project root
2. Copy the navbar and footer from an existing page
3. Register in the navigation menu
4. Add link in the navbar `<a>` tags

## Features Inventory
- [List all features with brief descriptions]

## Maintenance Tips
- [Any common maintenance tasks]
- [Troubleshooting notes]

## AI-Assisted Updates
To update this site, tell your AI agent:
> "Update [project name]" and reference `[project_name]_operations.md`
```

---

## Rules

1. Never use external paid APIs unless the user explicitly requests
2. Never add backend/database unless explicitly requested
3. All generated sites must work fully offline (no build step)
4. Every site must be responsive (mobile, tablet, desktop)
5. Operations manual is mandatory — do not skip Phase 3
