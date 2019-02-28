# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [v0.1.0] - 2019-02-28

Initial release.

### Added

- Sync/async providers.
  - Providers are named after their function, unless `name` is given.
- Sync/async consumers.
- `function` and `session` scopes.
- Session-scoped generator providers.
- Lazy async providers (function-scoped only).
- Provider discovery: `@aiodine.provider`, `providerconf.py`, `discover_providers()`.
- Nested providers: providers can consume other providers.
- Use the `aiodine` module directly or create a separate `Store`.

[unreleased]: https://github.com/bocadilloproject/aiodine/compare/v0.1.0...HEAD
[v0.1.0]: https://github.com/bocadilloproject/aiodine/releases/tag/v0.1.0