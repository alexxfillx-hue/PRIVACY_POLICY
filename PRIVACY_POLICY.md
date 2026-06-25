# Privacy Policy — Tanki Script Detector

**Last updated:** [25.06.2025]

## What this extension does

Tanki Script Detector scans pages on tanki.online and tankionline.com for
signs of third-party scripts, cheat tools, or browser extensions that modify
the page (for example, hooking WebSocket or console APIs). It runs an initial
scan when the page loads, and repeats the scan automatically roughly every
2.5 minutes while the tab stays open.

## What data is collected

When a scan completes, the extension collects:

- **Scan verdict** (CLEAN or DETECTED) and the technical signals that led to it
  (e.g. whether WebSocket was hooked, which browser APIs were modified).
- **The in-game nickname** visible in the player's own game HUD, used only to
  match the scan to the correct Discord account.
- **Diagnostic code excerpts** of any hook found (for example, the modified
  WebSocket function's source), used to identify which third-party tool was
  responsible.
- A **timestamp** of the scan.

The extension does **not** collect browsing history, passwords, payment
information, or any data from sites other than tanki.online/tankionline.com.

## Where this data goes

Scan results are sent automatically to a Discord webhook controlled by the
[Sandbox Ranked] Discord server's moderation team. This data is
used solely to verify that a player's anti-cheat checker is active before
they join a matchmaking room on that Discord server, and to alert moderators
if a cheat tool is detected.

This extension is built for a specific Discord community and is not intended
for general use outside that community's moderation workflow.

## Data retention

Scan data is stored by the Discord server's moderation bot for as long as
needed to verify checker status (a rolling few minutes) and, in the case of a
detected cheat, retained in a moderation log for review purposes.

## Your choices

You can disable or remove this extension at any time via
`chrome://extensions`. Disabling the extension stops all scanning and data
transmission immediately.

## Contact

Questions about this extension or its data practices: [shtaaavo@gmail.com]
