# Working with the judging snapshot

- Start with [README](README.md) and the [Unity project context](docs/UnityProjectContext.md).
- Keep Unity asset GUIDs, roster IDs, and multiplayer wire IDs stable. The embedded Core package owns the engine-free rules shared with the .NET tests.
- Keep private settings, local profiles, generated files, playtest logs, and player builds out of commits. Use a separately configured service deployment for online testing.
- Run the .NET Core tests and use focused Unity checks for changed behavior. Record the revision, platform, and what was exercised.
- Preserve author and license notices. Use [Credits](docs/CREDITS.md) for public-facing attribution.
