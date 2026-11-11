# Wows Battle Tracker Agent

## Overview

The Battle Tracker agent is a Windows service that runs on the PC where you play World of Warships. When a battle
starts, it reads the battle information the game writes to its replays folder and sends it to
[Wows Battle Tracker](https://www.wows-battle-tracker.com/), where it's stored and can be searched. Nothing else on
your PC is read or sent.

The same instructions are on the site's [Get the agent](https://www.wows-battle-tracker.com/agent) page.

## Table of Contents

- [Download](#download)
- [Installation](#installation)
- [Start the service](#start-the-service)
- [Removing it](#removing-it)
- [Questions and data requests](#questions-and-data-requests)
- [Warranty](#warranty)
- [Credits](#credits)

## Download

[BattleTrackerAgent-2.0.2.1.msi](https://github.com/CoryGM/wows-battle-tracker-downloads/raw/main/Downloads/BattleTrackerAgent-2.0.2.1.msi)
(29 MB)

MD5 checksum: `BC2A35531AB781ACD75B7110DA6E60AD`

The link downloads the installer directly.

## Installation

The agent needs 64-bit Windows. It's built on .NET 10, and the runtime is included in the installer, so there's
nothing else to install first.

1. Open the downloaded file and choose **Install**.
2. If World of Warships isn't installed in `C:\Games\World_of_Warships`, tell the agent where it is. Open
   `C:\Program Files\WowsBattleTracker\BattleTrackerAgent\appsettings.json` in a text editor and change
   `"WowsDirectory"` to your game folder, with double backslashes between folders, for example
   `"D:\\Games\\World_of_Warships"`.

## Start the service

The installer sets the service to start with Windows, but doesn't start it. Restart your PC, or start it now:

1. Press the Windows key, type **Services** and open it.
2. Find **Wows Battle Tracker Agent**, right-click it and choose **Start**.

Its status changes to "Running". You only need to do this once. After that, play a battle, and it shows up on the
site's dashboard a few seconds after the battle starts.

## Removing it

Uninstall **BattleTracker Agent** from Windows Settings > Apps, like any other program. The service is removed with it.

## Questions and data requests

Open an issue in this repository for questions about the agent or the site, or to have your account deleted.
Issues are public, so please don't include your email address or other personal details. See the site's
[Privacy Policy](https://www.wows-battle-tracker.com/privacy-policy) and
[Data Deletion Policy](https://www.wows-battle-tracker.com/data-deletion-policy).

## Warranty

This project is provided "as-is" and without any actual or implied warranty. Usage is at your own risk. By downloading
and installing the agent you agree to this risk.

## Credits

This project was created by Warcaster64.
