# Contributing Guidelines for arena-animation

> [!IMPORTANT]
> **No emoji in documentation, code comments, commit messages, or GitHub issue/PR titles and descriptions.**
> Write plain text. Emoji render inconsistently across editors, terminals, diffs, and generated release notes, and add nothing a plain word does not. This applies to all contributors, including automated/agentic coding tools. Icons in the software's own user interface are fine, but they must follow the project's existing conventions for UI icons.

## CI & Dependency Management Conventions
- **GitHub Actions Tag SHA Pinning**: All GitHub Action references in `.github/workflows/` MUST be pinned to the exact commit SHA of the official release tag (e.g., `uses: actions/checkout@11d5960a326750d5838078e36cf38b85af677262 # v4.4.0`).
- **Inline Version Comments**: The inline comment next to the SHA MUST specify the exact tag version used. This enables Dependabot to recognize the release version, generate human-readable SemVer PR titles (`from X.Y.Z to A.B.C`), and automatically update version comments during upgrades.