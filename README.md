# Magic Lantern Installer

The easy way to put [Magic Lantern](https://www.magiclantern.fm/) on your Canon EOS M, by [Filmatura](https://filmatura.com). Pick your SD card, and it walks you through the rest, with short videos showing what to do on the camera.

**Download it at [filmatura.com/pages/magic-lantern-installer](https://filmatura.com/pages/magic-lantern-installer)** (Mac and Windows, free).

## What it does

- Only lists removable, SD-card-sized drives, so your computer's own disk is never an option
- Formats the card and, if your camera isn't on Canon firmware 2.0.2 yet, puts the update on it and shows you how to run it on the camera
- Downloads the latest version of the build you choose and copies it to your card
- Lets you add a custom boot logo
- Has a Quick Mode for when you already know the drill

## If it won't open the first time

The installer isn't signed with a paid Apple or Microsoft certificate yet, so your computer may block it on first launch.

**Mac:** if macOS says the app "can't be opened" or "is damaged", move it to your Applications folder, open Terminal and run:

```
xattr -cr "/Applications/Magic Lantern Installer.app"
```

Then open it as usual. You only need to do this once.

**Windows:** on the blue "Windows protected your PC" screen, click **More info**, then **Run anyway**.

## Builds & credits

The installer doesn't change Magic Lantern itself. It installs builds made by the EOS M community, and the build list in the app is updated over time. It currently includes:

| Build | Source | By |
|---|---|---|
| Filmatura's Crop Mood *(default)* | [Filmatura/crop-mood-filmatura](https://github.com/Filmatura/crop-mood-filmatura) | Filmatura, forked from Amit's build |
| Amit's Crop Mood Slim | [Amit199167/Crop-mood-eosm-slim-gui](https://github.com/Amit199167/Crop-mood-eosm-slim-gui) | [Amit Kattal](https://github.com/Amit199167) |
| Crop Mood FilmGate (Beta) | [shaneintherain/Crop-mood-eosm-filmgate](https://github.com/shaneintherain/Crop-mood-eosm-filmgate) | [shaneintherain](https://github.com/shaneintherain), forked from Amit's build |
| Crop Mood + Danne Tweaks | [Magic Lantern forum thread](https://www.magiclantern.fm/forum/index.php?topic=27084.25) | Danne |
| Crop Mood | [Magic Lantern forum thread](https://www.magiclantern.fm/forum/index.php?topic=26851.0) | Bilal |

Huge thanks to Bilal, Danne, Amit and shaneintherain for building these for the EOS M, and to the [Magic Lantern](https://www.magiclantern.fm/) team for years of work on the firmware itself.

### License

Magic Lantern and every build above are licensed under **[GNU GPL v2](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)**, and each build's source is at the link in the table. Most builds are downloaded straight from their authors' GitHub releases. The Danne Tweaks and Crop Mood builds ship inside the installer, unmodified.

The installer itself is a separate, closed-source program by Filmatura.

Magic Lantern is unofficial software, not made or approved by Canon. Installing it may affect your warranty and is at your own risk. Filmatura isn't affiliated with the Magic Lantern project.

---

This repository holds the installer's release files and update feed, plus its remotely editable content in [`content/`](content/). To get the installer, use the download page above. The installer is proprietary - see [LICENSE](LICENSE). Copyright (c) 2026 Filmatura.
