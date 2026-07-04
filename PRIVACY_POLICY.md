# Privacy Policy — Tanki Script Detector

**Last updated:** 04.07.2026

## What this extension does

Tanki Script Detector scans pages on tanki.online and tankionline.com for
signs of third-party scripts, cheat tools, or browser extensions that modify
the page (for example, hooking WebSocket or console APIs). It runs an initial
scan when the page loads, and repeats the scan automatically roughly every
1–1.7 minutes (randomized) while the tab stays open, including while the tab
is in the background.

Before any scan or data transmission happens, the extension shows a one-time
consent screen in its popup. Scanning and sending data starts only after you
accept it, and your choice is remembered so the screen isn't shown again.

## What data is collected

When a scan completes, the extension collects:

- **Scan verdict** (CLEAN or DETECTED) and the technical signals that led to
  it (e.g. whether WebSocket was hooked, which browser APIs were modified,
  suspicious iframe/Worker creation, synthetic input events).
- **The in-game nickname and/or account UID** visible in the player's own
  game HUD/footer, used only to match the scan to the correct Discord
  account.
- **Diagnostic code excerpts** of any hook found (for example, the modified
  WebSocket function's source), used to identify which third-party tool was
  responsible.
- **Basic browser/device information**: browser name and version, operating
  system platform, language, GPU/CPU-adjacent figures exposed by the browser
  (`hardwareConcurrency`, `deviceMemory`), number of installed plugins,
  screen resolution and pixel ratio, and the full user agent string. This is
  used to tell apart different browsers/devices when reviewing a report, not
  to track you across sites.
- A **timestamp** of the scan.

The extension does **not** collect browsing history, passwords, payment
information, keystrokes/mouse movement content, or any data from sites other
than tanki.online/tankionline.com.

## Where this data goes

Scan results are sent automatically, over HTTPS, to a server operated by the
[Sandbox Ranked] Discord server's moderation team
(`tanki-checker.nrtranked.workers.dev`), which then forwards the result into
a private, moderator-only channel on that Discord server. This data is used
solely to verify that a player's anti-cheat checker is active before they
join a matchmaking room on that Discord server, and to alert moderators if a
cheat tool is detected.

The scan verdict and diagnostic details are **never shown back to the player**
inside the extension itself — the popup only ever indicates that the checker
is running, so that a cheat tool cannot use the extension's own UI to learn
which of its signals was detected.

This extension is built for a specific Discord community and is not intended
for general use outside that community's moderation workflow.

## Data retention

Scan data is stored by the Discord server's moderation bot for as long as
needed to verify checker status (a rolling few minutes) and, in the case of a
detected cheat, retained in a moderation log for review purposes. Reports of
a detected cheat may be held briefly (up to 15 minutes) awaiting independent
corroboration from other reports before a moderator is alerted, to reduce
the chance of a single fabricated report being acted on.

## Your choices

You can decline the consent screen (no data is collected or sent), and you
can disable or remove this extension at any time via `chrome://extensions`.
Disabling the extension stops all scanning and data transmission
immediately.

## Contact

Questions about this extension or its data practices: [shtaaavo@gmail.com]
