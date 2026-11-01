# Tooling and validation notes

This profile was prepared with the tools available in the Codex environment on 1 November 2026.

## Skills

- **GitHub Profile README** (`showxu/skills`, installed at user scope): used as the profile-specific guide for GitHub rendering, responsive banner proportions, badges, and post-publish checks. Its source was previewed with `gh skill preview` before installation. Installed version: `fc3529f199d43d1df6968bfc682220d3e75a2c4b`.
- **Playwright** (already installed): used for browser-based desktop and narrow viewport inspection of the published profile.
- **Skill Creator** and **Skill Installer** (preinstalled Codex skills): used to create and validate the reusable `github-profile-curator` skill, and to discover and install the profile-specific guide.
- **`github-profile-curator`** (created at `~/.codex/skills/github-profile-curator`): adds evidence, privacy, and publication-scope checks specific to personal developer profiles. Its structure was validated with the Skill Creator validator.
- **Project ERP skills** (`enterprise-ui-designer`, `erp-functional-analyst`, `financial-controls-qa`, `playwright-acceptance-qa`): available locally. The ERP workflow review skills informed verification of ProcureFlow claims; application UI skills were not needed to author a GitHub profile.

## GitHub and browser tools

- GitHub CLI (`gh`) authenticated as `Aadersh2996`; repository inspection, profile-repository creation, commits, pushes, GraphQL pins, and public metadata checks use the CLI/API.
- `gh skill search`, `gh skill preview`, and `gh skill install` are available in this installed CLI. The skill-management commands are in preview; use `gh skill <command> --help` to inspect the local version's syntax.
- The Playwright CLI is available for checking the rendered profile. The Codex computer-use browser surface is disabled by current Work settings in this session; GitHub's rendered page remains the source of truth for final visual review.

## Visual assets and validation

- The banner, divider, and project cards are hand-authored SVGs in `assets/`; no image-generation tool was exposed in the available tool inventory, so the visuals use native vector artwork.
- ProcureFlow screenshots link to the actual public image files in its repository. Profit Forensics Engine currently documents screenshot placeholders; the profile uses an original illustrative diagram and labels it as such.
- SVG files can be checked as XML and rendered in the browser. Markdown can be checked with GitHub's Markdown rendering API; links and images must also be checked on the public profile after publishing.

## Privacy and scope

- The profile includes the user's explicitly provided name and username, public project links, and no email, phone number, private repository, credential, machine path, visitor counter, or unsupported achievement.
- No global Codex configuration or hooks were changed. The current Codex configuration contains no hook definitions.
- No extra MCP server or plugin was installed for this task.
