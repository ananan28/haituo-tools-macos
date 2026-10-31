# Haituo Tools for macOS (Apple Silicon)

This repository builds the Python/PYW tools from the migration source archive.

## Source archive expected
Place `haituo-source-only.zip` in the repository root. It must contain `scripts/`, `wrappers/`, `build_macos.sh`, `requirements-macos.txt`, and `mac_preflight.py`.

The original Windows-only `新筛姓名.exe` is excluded because it has no source code and cannot be converted into a native Mac app as-is.

## Build
Pushing the source archive triggers GitHub Actions on an Apple Silicon macOS runner. The workflow builds the `.app` bundles and `.dmg`, then uploads them as a workflow artifact.

Build artifacts are unsigned and not notarized. On first launch macOS may require Finder > right-click > Open.
