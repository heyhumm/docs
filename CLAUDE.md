# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the Mintlify documentation site for **hum-app**. The hum-app source code lives in the ABI project (`~/src/abi/`), not in this repository. When documenting features or APIs, reference the ABI codebase for implementation details.

## Development Commands

```bash
# Install Mintlify CLI globally (required for local development)
npm i -g mint

# Start local development server (runs at http://localhost:3000)
mint dev

# Update Mintlify CLI to latest version (useful if dev server has issues)
mint update
```

## Architecture

- **docs.json**: Main configuration file defining navigation structure, theming, and site settings
- **MDX files**: Documentation pages with YAML frontmatter
- **snippets/**: Reusable content snippets that can be included in other pages
- **api-reference/**: API documentation including OpenAPI spec (`openapi.json`)

## Content Standards

- Document just enough for user success—not too much, not too little
- Search for existing information before adding new content; avoid duplication
- Check existing patterns for consistency
- Start by making the smallest reasonable changes
- Make content evergreen when possible

## Writing Standards

- Second-person voice ("you")
- Prerequisites at start of procedural content
- Test all code examples before publishing
- Match style and formatting of existing pages
- Language tags on all code blocks
- Alt text on all images
- Relative paths for internal links

## Frontmatter Requirements

Every MDX file must include:
- `title`: Clear, descriptive page title
- `description`: Concise summary for SEO/navigation

## Git Workflow

- NEVER use --no-verify when committing
- Ask how to handle uncommitted changes before starting
- Create a new branch when no clear branch exists for changes
- Commit frequently throughout development

## Do Not

- Skip frontmatter on any MDX file
- Use absolute URLs for internal links
- Include untested code examples
- Make assumptions—always ask for clarification
