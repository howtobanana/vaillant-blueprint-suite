# Git Workflow (Vaillant Blueprint Suite)

This repository is version-controlled to prevent accidental loss during refactors.

## Active Suite Blueprints
- `blueprints/vaillant_heizungs-steuerung.yaml`
- `blueprints/vaillant_geofencing.yaml`
- `blueprints/vaillant_lüftungs-steuerung.yaml`
- `blueprints/vaillant_system-diagnose.yaml`

## Safety Rules
- Commit before and after every substantial refactor.
- Keep one logical change per commit.
- Tag stable checkpoints before risky rewrites.
- Do not rewrite files from scratch unless explicitly intended.

## Recommended Flow
1. Create a work branch from `main` (use prefix `codex/`).
2. Make targeted edits.
3. Validate YAML syntax.
4. Commit with a clear message.
5. Merge back to `main` only after test/validation.

## Quick Commands
```bash
git status
git diff
ruby -e "require 'yaml'; YAML.load_file('blueprints/vaillant_heizungs-steuerung.yaml'); puts 'YAML OK'"
git add -A
git commit -m "Describe change"
```

## Recovery
- List tags: `git tag`
- Restore a file from a tag: `git checkout <tag> -- <file>`
