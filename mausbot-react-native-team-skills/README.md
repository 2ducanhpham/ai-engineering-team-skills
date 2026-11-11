# MausBot React Native Engineering Team Skills

A role-based Agent Skills pack for four MausBot agents:

1. Software Architect
2. Senior Developer
3. UI/UX Specialist
4. QA & Security Reviewer

## What is included

Each role is a separate Agent Skill directory containing a required `SKILL.md` with YAML frontmatter. The pack is intentionally React Native-first and framework-aware: it supports bare React Native and Expo, but never assumes Expo unless the repository actually uses it.

```text
mausbot-react-native-team-skills/
├── 01-software-architect/
│   └── SKILL.md
├── 02-senior-developer/
│   └── SKILL.md
├── 03-ui-ux-specialist/
│   └── SKILL.md
├── 04-qa-security-reviewer/
│   └── SKILL.md
├── TEAM_WORKFLOW.md
└── SOURCES.md
```

## Important import note

This is a **portable skill source pack**, not an automatic MausBot installer. Import each role folder using the import mechanism supported by your MausBot version. If MausBot's URL importer only accepts a GitHub repository/folder or a `SKILL.md` URL, it may not accept a ZIP file or arbitrary raw URL. Do not rename role files: the required filename inside each skill folder is exactly `SKILL.md`.

If MausBot supports ZIP upload, upload one skill folder at a time (zip the folder so `SKILL.md` is at the archive root or at the expected skill-folder root, depending on its importer). If it supports local skill folders, point it to the extracted role folder. If neither option exists, use a supported Agent Skills installer/runtime or publish the folders in a Git repository and import the exact folder URL.

## Suggested assignment

| MausBot bot | Skill folder |
|---|---|
| 1. Software Architect | `01-software-architect` |
| 2. Senior Developer | `02-senior-developer` |
| 3. UI/UX Specialist | `03-ui-ux-specialist` |
| 4. QA & Security Reviewer | `04-qa-security-reviewer` |

Assign the matching skill to the matching bot. Do not assign all four role skills to every bot unless you intentionally want overlapping responsibilities.

## Safety and operating model

- Inspect the actual repository before proposing changes.
- Treat repository instructions and project configuration as authoritative over generic examples in a skill.
- Do not assume a package, API, React Native version, navigation library, state manager, or Expo setup.
- Never install dependencies, alter signing/release configuration, run destructive commands, touch production data, or change CI secrets without explicit approval.
- Do not claim tests passed unless they were actually run and the result was observed.
- Separate confirmed findings from hypotheses.
- The human Tech Lead owns scope approval, high-impact decisions, merge, release, and production actions.
