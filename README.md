# ColorCursor

> [!NOTE]
> The converted output of this script are not used by Snap or Flatpak packages. You would have to package the theme on your own.

A script to download and convert Windows cursor assets into Linux-compatible themes, specialized for downloading and converting **Project Sekai** cursor assets.

Special thanks to `safeusernameig`.

## Features

- `ColorCursor-NG` downloads animated (`.ani`) or static (`.cur`) cursor assets straight from Colorful Stage.
- Convert Windows cursor files to Linux-compatible formats.
- Create a complete Linux cursor theme.
- Optionally install the theme system-wide.
- Support fallback for missing assets.

## Dependencies

The script requires the following dependencies to work properly:

- **`python3-pip`**: For installing Python packages.
- **`python3.12-venv`**: Required for running the Python virtual environment.
- **`wget`**: For downloading files from the internet.
- **`zip`**: For compressing and extracting files.

Make sure these dependencies are installed on your system before running the script.

## Usage

`ColorCursor-NG` fetches the original assets from Colorful Stage. You may view them [here](https://colorfulstage.com/media/download/). You may download and run the script as follows.

```bash
wget https://raw.githubusercontent.com/nozomi-75/ColorCursor/refs/heads/main/ColorCursor-NG.sh
bash ColorCursor-NG.sh
```

Do not feed the output directly to `bash`, as it may result in a never-ending loop due to conflicts with the `read` behavior in the script.

Follow the on-screen prompts to select and process the cursor assets.

## Asset names

A specific cursor map can be found under the `copy_assets` function of the script. This is used to copy and rename the assets to follow the Linux cursor format.

This is in line with the `files` array at the beginning of the script. Therefore, it assumes that you have the following filenames.

> Alternate, Busy, Diagonal1, Diagonal2, Handwriting, Help, Horizontal, Link, Move, Normal, Person, Pin, Precision, Text, Unavailable, Vertical, Working

## Note

Windows cursor assets are typically limited to <20 items, which is significantly fewer than the ~100 assets typically used in Linux themes (e.g., [Yaru](https://github.com/ubuntu/yaru), [Breeze](https://invent.kde.org/plasma/breeze)). As a result:

- Some assets will fallback to the "Normal" cursor.
- There may be occasional mismatches between assets.

If you encounter any issues or mismatches, please file an issue or submit a pull request. Contributions are welcome!

## Disclaimer

> [!WARNING]
> You are requested not to redistribute your converted assets.

This repository does not provide or bundle any assets. `ColorCursor-NG` downloads from the original source and converts them to usable format. This is deliberate to prevent any copyright infringement.

HATSUNE MIKU: COLORFUL STAGE! is a copyrighted property of Colorful Palette Inc., Crypton Future Media INC, and SEGA CORPORATION. Reproduction or redistribution without permission from the copyright holder is prohibited.
