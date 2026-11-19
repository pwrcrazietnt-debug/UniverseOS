# Security Policy

## Scope

UniverseOS is currently a planning repository and does not yet ship an operating-system image. This policy will be expanded as executable components are introduced.

## Reporting a vulnerability

Please do not publish exploitable details in a public issue. Contact the repository maintainers through GitHub's private vulnerability reporting feature if it is enabled. If it is not enabled, ask a maintainer for a private reporting channel without including exploit details in public.

## Security priorities

- Unknown packages must never be executed for identification.
- Installation must require clear user consent.
- Privileged operations must be explicit and auditable.
- Runtime and app data should be isolated from core system files.
- Updates should be authenticated and recoverable.
- Logs and reports must avoid leaking credentials, tokens, or personal data.

## Current status

There is no released UniverseOS image or supported production build at this time. Do not install experimental operating-system images on devices containing important data.
