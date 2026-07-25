# Andres Marrugo — contenido en español

This repository contains the Spanish half of the bilingual Hugo site.

## Write from iPhone or iPad

1. Open this repository on GitHub and press `.` to launch github.dev.
2. Add or edit a file in `content/es/posts/`.
3. Commit the change to the `master` branch.

The English repository then rebuilds and publishes the complete bilingual
site automatically. Use `archetypes/default.md` as the front-matter pattern
for a new post. Images belong in `static/images/` and can be referenced as
`/es/images/filename.jpg`.

## One-time connection

Create a fine-grained personal access token that can trigger Actions in
`agmarrugo/agmarrugo.github.com`, then save it in this repository under
**Settings → Secrets and variables → Actions** as `ENGLISH_REPO_PAT`.
