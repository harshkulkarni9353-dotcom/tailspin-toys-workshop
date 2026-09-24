---
description: 'Shared TypeScript, documentation, and comment standards'
applyTo: '**/*.{ts,astro}'
---

# Coding Standards

## Comments and documentation

- Comment intent, constraints, and non-obvious decisions — explain **why** the code exists rather than restating **what** the code already says.
- Prefer clear names and structure over comments that narrate straightforward control flow.
- Keep comments current. Update or remove a comment whenever the related behavior changes; an outdated comment is a bug.
- Use TSDoc (`/** ... */`) for public TypeScript APIs. Exported functions in `db/` and `src/lib/` must document their purpose, every parameter (including injectable `db` arguments), and their return value.
- Reusable `.astro` components must document their `Props` interface, including the purpose and constraints of each non-obvious prop. Page-only frontmatter does not need a component contract.
- Use inline comments only for local intent or a non-obvious constraint. Do not add comments that duplicate a type, expression, or markup label.

## TypeScript formatting

- Use two spaces for indentation, single-quoted strings, semicolons, and trailing commas in multiline lists.
- Use explicit parameter and return types for exported functions and public helpers.
- Prefer `interface` for object contracts and `type` for unions, intersections, and aliases that are not extended.
- Keep formatting consistent with the repository ESLint configuration; do not disable a formatting or documentation rule without explaining the exception.
