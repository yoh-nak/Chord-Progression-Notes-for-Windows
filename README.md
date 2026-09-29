# Chord Progression Notes for Windows

Chord Progression Notes is a lightweight Windows desktop application for editing, previewing, transposing, opening, and saving chord progression and lead-sheet files.

Supported formats:

- ChordPro
- Chord Over Lyrics
- MusicXML
- ABC notation

This repository currently provides a Windows installer builder script.

The included `.bat` file builds the application and creates a normal Windows installer:

`Chord-Progression-Notes-Setup-1.1.7.exe`

Once the installer has been created, end users only need the generated `.exe`.

Node.js and npm are only required for building the installer.

## Requirements

To build Chord Progression Notes, you need:

- Windows 10 or Windows 11
- Node.js LTS
- npm
- At least about 5 GB of free disk space during the build process
- An internet connection for downloading Electron and required npm packages

Node.js can be downloaded from:

https://nodejs.org/

npm is included with Node.js.

## How to Build

1. Download:

`BUILD_Chord_Progression_Notes_v1.1.7_Installer.bat`

2. Place the BAT file on a drive with enough free disk space.

For example:

`E:\`

This is recommended if your C: drive has limited free space.

3. Double-click:

`BUILD_Chord_Progression_Notes_v1.1.7_Installer.bat`

4. The script will automatically:

- check available disk space
- create a temporary build folder
- prepare the application source files
- run npm install
- download Electron and required dependencies
- build the Windows application
- create the installer executable

5. When the build completes successfully, the installer will be created on your Desktop:

`Chord-Progression-Notes-Setup-1.1.7.exe`

## Important

Node.js and npm are required only for building the application.

They are NOT required after the installer has been created.

The final installer:

`Chord-Progression-Notes-Setup-1.1.7.exe`

can be distributed and installed like a normal Windows application.

Users installing the generated EXE do not need:

- Node.js
- npm
- the BAT file
- the source code
- Electron installed separately

Everything required to run the application is included in the generated installer.

## Disk Space

Electron applications require a relatively large amount of temporary disk space while building.

At least approximately 5 GB of free space is recommended.

The build script uses the same drive where the BAT file is located.

If your C: drive is nearly full, move the BAT file to another drive such as:

`D:\`

or

`E:\`

and run it from there.

## Supported File Formats

### ChordPro

Supported extensions:

- `.chordpro`
- `.pro`
- `.cho`
- `.crd`

Features include:

- chord and lyric parsing
- section headings
- `start_of_*` directives
- `end_of_*` directives
- chord transposition
- lead-sheet preview

### Chord Over Lyrics

Supported extension:

- `.txt`

Traditional chord-above-lyrics text files can be opened and edited directly.

### MusicXML

Supported extensions:

- `.musicxml`
- `.xml`

Chord, lyric, metadata, tempo, key, and section information can be extracted for lead-sheet preview.

### ABC notation

Supported extension:

- `.abc`

ABC metadata, chord symbols, sections, and lyrics can be displayed as a simplified lead sheet.

## Features

- Open and save supported files
- Drag and drop files directly into the editor
- Edit / Split / Preview views
- Lead-sheet style preview
- Editor chord transposition
- Preview-only transposition
- ChordPro start and end directive support
- Font zoom controls
- File format detection
- Windows desktop application
- Single Windows installer after building

## Keyboard Shortcuts

- `Ctrl + O` — Open file
- `Ctrl + S` — Save
- `Ctrl + Shift + S` — Save As
- `Ctrl + N` — New document
- `Ctrl + +` — Increase font size
- `Ctrl + -` — Decrease font size
- `Ctrl + 0` — Reset font size to 100%

## Installation

After building, run:

`Chord-Progression-Notes-Setup-1.1.7.exe`

The application can then be managed from:

Windows Settings  
→ Apps  
→ Installed apps  
→ Chord Progression Notes

It can be uninstalled normally from Windows.

npm is NOT required for uninstalling the application.

## Windows Security Notice

The installer is currently unsigned.

Because of this, Windows SmartScreen or User Account Control may display:

`Unknown publisher`

The application metadata identifies the author as:

`Yohsuke Nakano`

A trusted Windows code-signing certificate is required for Windows to display a verified publisher name.

## Development

The application is built using:

- JavaScript
- Electron
- HTML
- CSS

The Windows installer is created with electron-builder.

## Author

Yohsuke Nakano

GitHub:

https://github.com/yoh-nak
