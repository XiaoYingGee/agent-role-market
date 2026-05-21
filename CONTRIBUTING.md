# Contributing

Contributions are welcome when they keep this repository tool-agnostic and role-oriented.

## Role Pack Rules

- Keep each role narrowly scoped.
- Do not include private identifiers, secrets, workspace paths, user handles, channel IDs, or vendor-specific commands.
- Define clear use cases and non-goals.
- Prefer checklists, input contracts, output contracts, and handoff rules over personality text.
- Do not copy third-party prompts verbatim.
- Add references only when they are used as inspiration or external reading.

## File Naming

- Use lowercase kebab-case.
- Place role packs under the most relevant role group directory.
- If a role spans many role groups, split it into smaller role packs.

## Review Checklist

- The role can be used by multiple agent tools.
- The role has required inputs and expected outputs.
- The role has completion criteria.
- The role does not require image understanding unless explicitly labeled as optional.
- The role does not assume a specific chat platform or task board.
