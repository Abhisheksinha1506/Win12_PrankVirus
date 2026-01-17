# Win12 Prank Virus (VBScript)

## Overview
This repository contains a simple **VBScript** file designed to be a harmless "prank virus." It simulates the installation of a fictional "Windows 12" operating system, mimicking a system crash/hack, and then displays a fake "Formatting all drives" sequence in the command prompt before initiating a system restart.

## Project Details
- **Type**: Prank Script
- **Language**: VBScript (`.vbs`)
- **Target**: Windows
- **Safety**: Harmless (visual effects only, though it does restart the computer).

## Script Behavior (`Windows 12 Install (64-bit).vbs`)
1. **Introduction**: Displays a message box welcoming the user to the "Windows 12 Installer."
2. **Fake Errors**: Simulates connection errors and file loading failures.
3. **CMD Takeover**: Opens `cmd.exe` and uses `SendKeys` to type out messages character-by-character ("You are being hacked!").
4. **Scare Tactics**: Changes the console color to green (Matrix style) then red. Prompts simulating unauthorized access.
5. **Fake Format**: Loops through a progress bar simulating the deletion of files and formatting of drives only using the `prompt` command (no actual data is deleted).
6. **Restart**: Executes `shutdown /r /t 0` at the very end to reboot the machine.

## Technical Notes
- **SendKeys**: The script relies entirely on `WshShell.SendKeys` to interact with the command prompt, which makes it fragile (if the user clicks away, the keys will be typed into whatever window is in focus).
- **No Persistence**: The script does not copy itself or add registry keys; it runs once and stops (after reboot).

## How to Explore
1. **Open the .vbs file**: Read the text to see the sequence of message boxes and `SendKeys` commands. **Do not double-click to run it** unless you want your computer to restart.
