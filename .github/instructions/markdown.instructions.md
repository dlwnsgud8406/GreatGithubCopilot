```instructions
---
description: 'Markdown documentation template and guidelines'
applyTo: '**/*.md'
---

## Markdown Documentation Template

This template provides guidelines for creating consistent, well-structured markdown documentation.

### Structure Guidelines

1. **Headings**: Use H2 (`##`) for main sections, H3 (`###`) for subsections. Avoid H1 in content as it may be generated from titles.
2. **Lists**: Use bullet points (`-`) or numbered lists (`1.`). Ensure proper indentation (2 spaces for nested items).
3. **Code Blocks**: Use fenced code blocks with language specification for syntax highlighting.
4. **Links**: Use descriptive link text with proper markdown syntax `[text](URL)`.
5. **Images**: Include alt text for accessibility `![alt text](image URL)`.
6. **Tables**: Use pipe syntax with proper alignment and headers.

### Style Conventions

- **Line Length**: Keep lines to ~80 characters for readability
- **Whitespace**: Use blank lines to separate sections
- **Code Examples**: Keep examples minimal and copy-pasteable
- **Consistency**: Follow established patterns within your documentation

### Optional Front Matter

If your publishing system requires metadata, include YAML front matter:

```yaml
---
title: Document Title
author: Author Name  
date: YYYY-MM-DD
tags: [tag1, tag2]
summary: Brief description
---
```

### Quality Checklist

- All links are valid and accessible
- Code examples include language specification
- Images have appropriate alt text
- Content is well-structured with clear headings
- Examples are tested and functional

```
- **Formatting**: Ensure that the content is properly formatted and structured according to the guidelines.
- **Validation**: Run the validation tools to check for compliance with the rules and guidelines.