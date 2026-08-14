# Split Skill Repositories Design

## Goal

Split two skills out of `Nahzzz77/aihanlab-skills` into independent public repositories while leaving `aihanlab-xhs-knowledge-notes` in the original repository.

## Target repositories

- `Nahzzz77/aihanlab-skills`: retain only `.codex/skills/aihanlab-xhs-knowledge-notes` as the distributed skill.
- `Nahzzz77/aihanlab-competitive-analysis`: contain the former `.codex/skills/aihanlab-competitive-analysis` directory at `.codex/skills/aihanlab-competitive-analysis`.
- `Nahzzz77/human-writing`: contain the former `.codex/skills/human-writing` directory at `.codex/skills/human-writing`.

All three repositories remain public. The original repository keeps its existing name and URL.

## History-preserving split

Create each new repository from a filtered copy of the original Git history. Preserve only the selected skill directory and rewrite its path to remain installable at `.codex/skills/<skill-name>`. This retains relevant authorship and commit history without copying unrelated skill files.

Do not alter the contents of the selected skill folders during the split. Preserve `SKILL.md`, `agents`, `references`, `scripts`, `dist`, `LICENSE`, `NOTICE`, and `VERSION` files when present.

## Original repository cleanup

After both new repositories are created and verified:

1. Remove `.codex/skills/aihanlab-competitive-analysis` from the original repository.
2. Remove `.codex/skills/human-writing` from the original repository.
3. Keep `.codex/skills/aihanlab-xhs-knowledge-notes` unchanged.
4. Rewrite the root `README.md` so it documents the remaining skill and links to both extracted repositories.
5. Retain historical planning and evaluation documents under `docs/`; they are part of the original repository history, not distributed skill contents.

## Verification

Before publishing the cleanup:

- Confirm each new repository is public and has `main` as its default branch.
- Compare every file and blob in each extracted skill against the corresponding source directory.
- Run the skill validator against all three skill directories.
- Run `human-writing/scripts/check_prose.py --help` or its supported smoke-test command to confirm the preserved executable still starts.
- Confirm the original repository contains exactly one directory beneath `.codex/skills`.
- Confirm README links resolve to the two new repositories.

## Safety and rollback

Create and verify the two new repositories before removing anything from the original repository. Perform the original cleanup in a dedicated commit so it can be reverted without affecting the new repositories. Do not delete or archive the original repository.
