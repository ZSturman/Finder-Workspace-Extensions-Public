# Finder Workspace Extensions

A native Mac companion that brings project status, work sessions and Better
Workspace capture actions into Finder.

[Download the signed 0.1.1 development preview](https://github.com/ZSturman/Finder-Workspace-Extensions-Public/releases/tag/v0.1.1) · [See real demos](https://zacharysturman.com/projects/finder-workspace-extensions)

## What it does

- Show cached project status and domain badges in Finder.
- Open project information, planning, work history and work sessions.
- Own project status, phase, domain, priority and maintenance; Better Workspace
  mirrors these through a bounded shared exchange, without shared databases.
- Open Capture Idea in Better Workspace’s shared composer. Better Workspace
  1.0.5 retains file-picking drafts, copies movie originals, keeps text on removal,
  shows full errors and requests notifications after completed idea saves.
- Export project-card snapshots for native Quick Look previews.

## Install and use

Requires macOS 14.4 or later. The download contains Apple silicon and Intel code.
Expand the ZIP, drag **Finder Workspace Extensions.app** to Applications, and open
it. Enable the desired extensions in System Settings → General → Login Items &
Extensions. Choose your workspace roots explicitly in the companion settings.
For shared capture, install [Better Workspace](https://github.com/ZSturman/Better-Workspace-Public/releases/tag/v1.0.5).

Right-click a project to choose a status or open planning. Capture Idea opens
Better Workspace; save there before quitting. Notification permissions belong to
Better Workspace. Do not disable Gatekeeper: this preview is Developer ID signed,
notarized and stapled.

## Architecture and privacy

The companion owns a private database. Finder reads cached snapshots and sends
bounded requests, keeping scans, database writes and network activity outside
Finder. Originals stay read-only unless a separate, explicit reviewed filesystem
action is accepted. Notion is optional. Neither app reads the other’s database.
This repository distributes binaries and public instructions; development history
and private evidence are maintained separately.

## Development preview limits

Routing/exchange tests and native builds pass. This release has not completed
clean-user installation, Intel runtime and every Finder, Services, login and
permission acceptance check. The Finder app is a direct download and has no
TestFlight/App Store edition. Better Workspace has a separate mobile Store app.

To remove it, disable its extensions and optional login startup, quit it, then move
only the application to Trash. Keep your project folders and private records.
