# Tooling and validation notes

This profile was prepared with the tools available in the Codex environment on 1 November 2026.

## Skills

- The Skill Installer's official curated catalog was queried; it did not include a GitHub profile authoring skill. `gh skill search` found the specialized community skill below, which was previewed before installation.
- **GitHub Profile README** (`showxu/skills`, installed at user scope): used as the profile-specific guide for GitHub rendering, responsive banner proportions, badges, and post-publish checks. `gh skill preview` was used before installation; GitHub CLI warned that this community skill is not verified by GitHub. Installed version: `fc3529f199d43d1df6968bfc682220d3e75a2c4b`.
- **Playwright CLI** (available through `npx`): used to open the published profile, inspect it at a 1280×900 desktop and 390×844 mobile viewport, capture screenshots, inspect rendered content, and check that profile images load without horizontal overflow.
- **Skill Creator** and **Skill Installer** (preinstalled Codex skills): used to create and validate the reusable `github-profile-curator` skill, and to discover and install the profile-specific guide.
- **`github-profile-curator`** (created in the user-level Codex skills directory): adds evidence, privacy, and publication-scope checks specific to personal developer profiles. Its structure was validated with the Skill Creator validator.
- **Project ERP skills** (`enterprise-ui-designer`, `erp-functional-analyst`, `financial-controls-qa`, `playwright-acceptance-qa`): available locally. The ERP workflow review skills informed verification of ProcureFlow claims; application UI skills were not needed to author a GitHub profile.

## GitHub and browser tools

- GitHub CLI (`gh`) authenticated as `Aadersh2996`; repository inspection and publication, profile name and bio updates, GraphQL pin inspection, and public metadata checks use the CLI/API.
- `gh skill search`, `gh skill preview`, and `gh skill install` are available in this installed CLI. The skill-management commands are in preview; use `gh skill <command> --help` to inspect the local version's syntax.
- The Playwright CLI is available for checking the rendered profile. The Codex computer-use browser surface is disabled by current Work settings in this session; GitHub's rendered page remains the source of truth for final visual review.
- The Codex configuration had the Browser, Chrome, computer-use, and unified computer-use plugins enabled, plus a Node REPL MCP server. The current Work setting disabled the connected browser surface, so the Playwright CLI was used for visual review. No additional plugin or MCP server was installed.
- GitHub's Markdown rendering API accepted the README as GFM. The public profile rendered with the full name, both featured projects, SVG assets, badges, and screenshots. The observed profile article fit its 390 px viewport without horizontal overflow; all README images reported loaded in Chromium.
- Browser review images are saved locally at `visual-review/profile-desktop.png` and `visual-review/profile-mobile.png`. The `visual-review/` directory is ignored by Git so screenshots do not become repository content.
- The authenticated GraphQL schema exposes `pinnedItems` and `pinnableItems` for inspection and reports six available slots, but its current mutation schema has no repository pin/unpin mutation. The pins require the profile UI: open the profile while signed in, select **Customize your pins**, choose `procureflow-p2p` and `profit-forensics-engine`, and save.

## Visual assets and validation

- The banner, divider, and project cards are hand-authored SVGs in `assets/`; no image-generation tool was exposed in the available tool inventory, so the visuals use native vector artwork. XML parsing and GitHub's own profile renderer both validated the SVGs.
- ProcureFlow screenshots link to the actual public image files in its repository. Profit Forensics Engine currently documents screenshot placeholders; the profile uses an original illustrative diagram and labels it as such.
- SVG files can be checked as XML and rendered in the browser. Markdown can be checked with GitHub's Markdown rendering API; links and images must also be checked on the public profile after publishing.

## Privacy and scope

- The profile includes the user's explicitly provided name and username, public project links, and no email, phone number, private repository, credential, machine path, visitor counter, or unsupported achievement.
- No global Codex configuration or hooks were changed. The current Codex configuration contains no hook definitions.
- No extra MCP server or plugin was installed for this task.
