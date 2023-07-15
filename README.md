# Wows Battle Tracker Agent

## Overview

This project is the Windows Service component that runs in the background and
monitors the World of Warships game directory for new game information. That 
game information is sent to the cloud service where it is stored in a 
searchable database. 

The website that exposes this battle search feature is located at [Wows Battle Tracker](https://wows-battle-tracker.calmwater-da218019.centralus.azurecontainerapps.io/).

## Table of Contents

- [Installation](#installation)
- [Start Service Manually](#start-service-manually)
- [Usage](#usage)
- [Download Instructions](#download-instructions)
- [Warranty](#warranty)
- [Credits](#credits)

## .NET 7.0 Runtime

This agent requires the .NET 7.0 runtime on the target computer. If you do not already have it, you will be prompted d
during the installation of the service. Simply download the installer and follow the instructions.

## Installation

To install this project, you will need to download the latest version of the installer from below on this page.

Once downloaded, click on the file and choose "Install".

If you have installed World of Warships in the default directory, you are all set to go.

If you have installed it in another location, you will need to tell the service where it is located. To do this

Find the World of Warships main installation directory. For example, the default installation will put it here: c:\Games\World_of_Warships.

Now find the configuration file for the Wow Battle Tracker Agent. The default location for this file is at:
c:\Program Files\WowsBattleTracker\BattleTrackerAgent\appsettings.json.

Open this file with your favorite text editor. Find the line that currently contains "WowsDirectory": "C:\\\\Games\\\\World_of_Warships". Replace the default directory location with the actual location of World of Warships you found earlier. You will need to include double slashes (\\\\) in the path to separate directories instead of single slashes.

## Start Service Manually

The agent is installed as a background Windows Service. It will start automatically the next time your computer is restarted.

If you wish to start the service right away, you can do so through the Services Control Panel in Windows. To access Services, hit the Windows Key and type in Services. You will see a result titled "Services" with double gears meshing icon. Click that and you get the list
of services currently running on your computer. 

Find the "Wows Battle Tracker Agent", right-click on it, and select "Start". If the service starts without error, you will see its 
status change to "Running" in the Control Panel.

## Usage

As a background Windows Service, there is nothing you need to do after the initial installation and setup. The service will silently run in the background and send the battle information to the cloud service. 

## Download Instructions

To download a specific file from this repository, you can click on the following link:

[BattleTrackerAgent-1.0.0.7.msi](https://github.com/CoryGM/wows-battle-tracker-downloads/tree/main/Downloads/BattleTrackerAgent-1.0.0.7.msi)

SHA256 Checksum: 18a37c38ba6608d5e3571a2af9ee5b0f924eefa6b481740fb52f57c674af4711

After you click on the link, it will take you to a page displaying the contents of the file. To download the file, click on the "Raw" button at the top of the file, then right click and select "Save As" to save the file to your desired location.

## Warranty

This project is provided "as-is" and without any actual or implied warranty. Usage is at your own risk. By downloading
and installing the agent you agree to this risk.

## Credits

This project was created by Warcaster64.