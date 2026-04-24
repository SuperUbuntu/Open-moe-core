# Moe Core Refactor Release Notes

## Summary

- Rebranded project-facing docs and metadata from MaiBot/MaiSaka/MaiCore to Moe Core.
- Rewrote README content around a pure core engine that pairs with external adapters.
- Added NOTICE with explicit MaiBot provenance and GPL-3.0 continuity.
- Removed original MaiBot community, deployment, QQ group, and NapCat acknowledgement sections from README docs.
- Updated visible startup, CLI, WebUI, statistics, and sample plugin strings where practical.
- Removed the NapCat adapter SDK test from the core distribution because NapCat/OneBot is no longer bundled here.

## Compatibility Notes

- Internal Python class/module names and SDK symbols such as `MaiBotPlugin` are left intact where renaming would risk breaking existing plugins or runtime imports.
- Some historical database and compatibility filenames remain unchanged for migration safety.
- Platform-specific adapters should be maintained and released outside this repository.
