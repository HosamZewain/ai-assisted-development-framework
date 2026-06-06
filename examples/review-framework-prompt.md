# Review AI Development Framework Prompt

Use this after the framework files are generated.

---

Review the AI Development Framework files you just created.

Check specifically:

1. `AGENTS.md` does NOT tell the AI to read all docs every time.
2. `CLAUDE.md` does NOT import all docs by default.
3. `docs/ai/context.md` is the only always-read shared context file.
4. Other docs are read conditionally based on task type.
5. Skills are under `.agents/skills/`.
6. Every `SKILL.md` has `name` and `description` metadata.
7. Every skill says to inspect only impacted modules, not the full repo.
8. No production code was changed.
9. No secrets or sensitive data were added.
10. `.DS_Store` and `__MACOSX/` are removed or ignored.
11. The docs are specific to this repository and not generic.
12. Any uncertain items are marked as `TBD - needs team confirmation`.

If anything is wrong, fix only the AI framework files.

Then summarize:

- Files updated
- Token-efficiency improvements
- Remaining TBD items
- Items needing Tech Lead review
