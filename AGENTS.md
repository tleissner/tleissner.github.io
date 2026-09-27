`themes/PaperMod` is a git submodule (see `.gitmodules`); in this repo it may be empty—run `git submodule update --init --recursive` before assuming Hugo templates/assets exist.
Do not edit `themes/PaperMod.broken.*` for normal changes; it’s not referenced by `config.yaml` (which sets `theme: PaperMod`).
`config.yaml` sets `params.assets.customCSS` to `css/custom.css`, but the only custom stylesheet here is `assets/css/extended/custom.css`—verify/fix the path when changing CSS.
This repo has no Hugo `content/` directory (only `archetypes/`, templates, and committed `public/`), so regenerating via Hugo may not reflect intended page/source changes—look for the real content source in the workspace.
Treat `public/` as generated output: it’s Hugo output and is gitignored (`.gitignore`), so avoid editing `public/*.html` directly.
Head/custom HTML in this repo should go into `layouts/partials/extend_head.html` (not theme templates).
The VS Code workspace (`www.till-leissner.de.code-workspace`) includes multiple sibling sites; make sure edits target the correct source folder for the site you’re changing.
