# 🎮 ROM Organizer

A simple Bash utility to automatically extract, organize and clean ROM collections for use with **ES-DE (EmulationStation Desktop Edition)**.

Originally created to simplify the repetitive process of importing ROM sets downloaded from preservation projects such as Redump, No-Intro and Myrient.

---

## ✨ Features

* 📦 Automatically extracts supported archive formats.
* 🎯 Detects ROM files from multiple consoles.
* 📁 Moves ROMs to the root directory (or future destination folders).
* 🗑 Removes extracted archives after successful extraction.
* 🧹 Recursively deletes empty folders left behind.
* ⚠ Interactive confirmation before destructive operations.
* 📊 Displays a summary of processed files.
* 💻 Written entirely in Bash with minimal dependencies.

---

## Supported archive formats

* ZIP
* 7Z
* RAR
* TAR
* TAR.GZ / TGZ
* TAR.XZ
* TAR.BZ2

---

## Supported ROM formats

| Console              | Extensions         |
| -------------------- | ------------------ |
| PlayStation          | iso, bin, cue, chd |
| PlayStation Portable | cso, pbp, elf      |
| Nintendo Wii         | rvz, wbfs, gcz     |
| Nintendo 3DS         | 3ds, cci, cia      |
| Nintendo DS          | nds                |
| Game Boy Advance     | gba                |
| Game Boy / Color     | gb, gbc            |
| NES                  | nes                |
| SNES                 | sfc, smc           |
| Nintendo 64          | n64, z64, v64      |
| Nintendo Switch      | xci, nsp           |

More extensions can easily be added by editing the `ROM_EXTENSIONS` array.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/Keel-Kuchiki69/ES-DE-Rom-Organizer.git
cd ES-DE-Rom-Organizer
```

Make the script executable:

```bash
chmod +x rom-organizer
```

(Optional) Install globally:

```bash
sudo mv rom-organizer ~/.local/bin/
```

Now the tool can be executed from anywhere:

```bash
rom-organizer
```

---

## Usage

Navigate to the directory containing your downloaded ROM archives.

Example:

```bash
cd ~/Downloads/Roms
```

Run:

```bash
rom-organizer
```

The script will:

1. Scan for supported archives.
2. Ask for confirmation.
3. Extract all archives.
4. Detect ROM files.
5. Move ROMs to the working directory.
6. Remove extracted archives.
7. Delete all empty folders.
8. Display a processing summary.

---

## Dependencies

The following tools must be installed:

* bash
* unzip
* p7zip (7z)
* unrar
* tar
* findutils

Most Linux distributions already provide these packages through their package manager.

---

## Roadmap

Planned features:

* [ ] Interactive console selection
* [ ] Automatic destination folders
* [ ] Multi-selection of archives
* [ ] `gum` interface support
* [ ] Dry-run mode
* [ ] Configuration file
* [ ] Logging
* [ ] Duplicate ROM detection
* [ ] Progress bar

---

## Why?

Managing ROM collections manually quickly becomes repetitive.

Many ROM preservation projects distribute games inside deeply nested directory structures:

```text
Minerva_Myrient/
└── Redump/
    └── Sony - PlayStation 2/
        └── Game.zip
            └── Game.iso
```

Extracting hundreds of archives manually, moving files and deleting leftover folders is both tedious and error-prone.

ROM Organizer automates the entire workflow in a single command.

---

## License

MIT License.

Feel free to modify the project to fit your own workflow.
