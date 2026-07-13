# Repository Publishing Checklist

## Product readiness

- [ ] The project has a clear name and one-line value proposition.
- [ ] Implemented and planned features are separated.
- [ ] The primary user and solved problem are stated.
- [ ] No fake metrics, testimonials, clients, awards, or performance claims are present.
- [ ] The application runs using the documented commands.
- [ ] Lint, test, and build commands have been executed.
- [ ] Broken links, images, badges, and routes have been removed.

## Security

- [ ] `.env`, `.env.local`, `.env.*`, credentials, sessions, keys, certificates, and dumps are ignored.
- [ ] `.env.example` contains names and placeholders only.
- [ ] No API key, password, token, private key, webhook secret, database URL, or personal information appears in the current tree.
- [ ] Git history was scanned with GitHub secret scanning or Gitleaks.
- [ ] Any previously exposed credential was rotated.
- [ ] Production IP addresses, SSH usernames, private paths, and internal logs are not documented unnecessarily.
- [ ] Screenshots contain no private data.

## Documentation

- [ ] README explains the project in the first five to eight lines.
- [ ] Installation commands match the actual package manager.
- [ ] Environment variables are accurate.
- [ ] User roles, architecture, limitations, and deployment are documented when relevant.
- [ ] Screenshots have alt text.
- [ ] The license claim matches the `LICENSE` file.
- [ ] Contact and ownership information are accurate.

## Visual presentation

- [ ] Social preview prepared at 1280 × 640.
- [ ] README hero uses a high-resolution asset.
- [ ] Desktop screenshot prepared at approximately 1440 × 900.
- [ ] Mobile screenshots use consistent proportions.
- [ ] Dashboard screenshot is included when it is a major capability.
- [ ] No irrelevant stock photography, distorted screenshots, or visual clutter is used.
- [ ] Arabic UI screenshots visibly demonstrate correct RTL behavior.

## GitHub metadata

- [ ] Repository name is descriptive and lower-case.
- [ ] Description states the user value and main capability.
- [ ] Website field contains a verified URL.
- [ ] Topics reflect the actual stack and domain.
- [ ] Default branch is correct.
- [ ] Visibility is appropriate.
- [ ] Archived status is accurate.
- [ ] Six strongest repositories are pinned strategically.

## Release

- [ ] Changes are split into focused commits.
- [ ] Version or release notes are added when appropriate.
- [ ] A clean clone was used to validate setup.
- [ ] The default branch remains buildable.
