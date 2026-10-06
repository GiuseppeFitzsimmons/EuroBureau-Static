# EuroBureau-Static

Static content for the EuroBureau platform, fetched at runtime so it can be
updated **without a redeployment**.

## Contents

| File       | Served at | Purpose                     |
|------------|-----------|-----------------------------|
| `terms.md` | `/terms`  | Terms & Conditions          |
| `faq.md`   | `/faq`    | Frequently Asked Questions  |

Files are Markdown. The platform fetches them at runtime from this repo's raw
URL (`raw.githubusercontent.com`) and renders them. Editing a file here and
pushing to `main` updates the live page after the platform's short cache
expires — no deploy required.

This repo is also wired into the main `DocumentServer` repo as a git submodule
at `static-content/` so the pinned content is versioned alongside the platform.
Runtime fetching does not depend on the submodule checkout; the submodule is for
reference and local development.
