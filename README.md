# Cheat Engine For Mobile — Releases

Official release downloads for **Cheat Engine For Mobile**, an Android app that runs your own
offline single-player games in a private virtual space and includes a memory editor
(scan, edit, freeze values). Author: **BriskBand**.

> **Made for single-player games.** Cheat Engine For Mobile changes values that live on your
> phone, so it is meant for games you play on your own. In online and PvP games, coins, health,
> ranks and other values are kept on the game's server: edits made on the phone are simply
> replaced by the server's values and do not reach other players. Please play fair
> in multiplayer games and use the app for your own single-player experience.

## Features

- **Games**: import an APK, or an XAPK / APKM / APKS bundle with split APKs and OBB data.
  Save backup and restore for each game. The game list warns about anti-cheat, probable
  online / server games and crashes. Games stay open while the screen is off.
- **Value search**: exact values, ranges (`10~20`), tolerance (`1.5+-0.1`), groups of related
  values, XOR-encoded values, and unknown-value scans (Up / Down / Changed / Same / by amount).
  Auto scan repeats Next Scan until the result count stops dropping.
- **Editing**: set and freeze values (also all results of a page at once), a Max button,
  block the code that writes a value (undoable), and pick a number straight from the game
  screen (short forms such as 18.2K become a search range).
- **History and saved addresses**: every edited address of the session and of earlier sessions,
  with how it was found. Named addresses are saved automatically and kept per game.
- **Pointer chains**: find chains (4 to 6 levels) that lead to a value and save them; they
  find the value again after the game restarts. Pointer rescan keeps only the chains that still
  work after a new match. Saved chains can be applied automatically when the game starts.
- **Game engines**: recognises Unity, Unreal, Cocos2d-x, Godot and libGDX. For Unity games
  you can browse classes, fields and live objects without scanning, list manager classes
  (static instance) and see encrypted fields.
- **In-game editor**: works on phones, tablets and foldables; the editor and the HUD button
  can be dragged, the editor collapses to one row and stays clear of the system bars and keyboard.
- **Forced ads**: forced (interstitial) ads in games inside CE are closed; rewarded ads still
  play normally. Can be turned off on the main screen.
- **Crash diagnosis**: when a game crashes inside CE, the game list shows the cause, and the
  local diagnostic report lists crashes, freezes and kills with details you can share.

Latest version: **1.11.0**. Each release lists its changes.

Which games work: see **[COMPATIBILITY.md](COMPATIBILITY.md)**.

## Download

Get the newest APK from **[Releases](../../releases/latest)**.

- Android 8.0 or newer, ARM64 (most phones) or x86_64.
- Install the new APK **over** the existing app. Do not uninstall first, or your
  imported games and saves inside CE are removed.

## Updates

Every time Cheat Engine For Mobile opens it checks `update.json` in the latest release. The update
notice shows the version on your device and the new version, and a Release page button opens
that release here. An internet
connection is needed for that check; after it passes, games can be played offline until CE is
opened again. When a newer required version exists, CE must be updated before it can be used.
`update.json` is signed, the APK is checked against its SHA-256, and Android only installs
updates signed with the same key.

## Scope

- No root. Works only on games imported into CE.
- Single-player and offline games only. Online, multiplayer and PvP games keep their values
  on a server, so they cannot be changed with this app.
- CE does not bypass anti-cheat, Play Integrity, licensing or Google sign-in. Games that
  use them may close inside CE; CE warns about known anti-cheat before launch.
- Games that download extra data through Google Play (Play Asset Delivery) may miss that
  data inside CE; import them as an XAPK / APKM bundle that includes it.

## Third-party software

The APK includes open-source components (BlackBoxReborn, Dobby, FreeReflection, xDL,
AndroidX, Kotlin). Their licenses are bundled in the app under `assets/licenses/`.
