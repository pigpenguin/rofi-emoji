## Goal of fork
Adding math symbols

## Progress
Turns out adding this manually is dull. I've added a very small subset of https://www.unicode.org/charts/PDF/U2200.pdf
I plan to finish it up but I got the symbols I needed right now added. Might try to find a place to pull them from
automatically as the original code does.

# Orignal read me below

# Rofi emoji plugin

An emoji selector plugin for Rofi that copies the selected emoji to the
clipboard.

## Usage

Run rofi like:

```bash
rofi -show emoji -modi emoji
```

| Key              | Effect                  |
|------------------|-------------------------|
| <kbd>Enter</kbd> | Copy emoji to clipboard |

**Note:** If you change your keybind for `kb-accept`, then your change will
also apply here.

## Screenshot

![Screenshot showing a Rofi window searching for emojis containing "uni", the
emoji for "Unicorn face" being selected](screenshot.png)

## Installation

**Dependencies**

| Dependency | Version      |
|------------|--------------|
| rofi       | 1.4 (or git) |

**Optional dependencies**

In order to actually use rofi-emoji some "adapters" need to be installed, as
appropriate for your environment.

| Dependency   | Notes                        |
|--------------|------------------------------|
| xsel         | For X11.                     |
| xclip        | For X11.                     |
| wl-clipboard | For Wayland. (**Untested!**) |

### Arch Linux

`rofi-emoji` can be installed via [AUR](https://aur.archlinux.org/):
[rofi-emoji](https://aur.archlinux.org/packages/rofi-emoji/)

### Compile from source

`rofi-emoji` uses autotools as build system. Download the source and run the following to install it:

```bash
$ autoreconf -i
$ mkdir build
$ cd build/
$ ../configure
$ make
$ sudo make install
```

## Emoji database

When installing the emoji database (`all_emojis.txt` file) is installed in
`$PREFIX/share/rofi-emoji`. The plugin will search `$XDG_DATA_DIRS` for a
directory where `rofi-emoji/all_emojis.txt` exists in. If the plugin cannot
find the data, make sure `$XDG_DATA_DIRS` is set correctly.

If it is unset it should default to `/usr/local/share:/usr/share`, which works
with the most common prefixes.

### Updating to a newer version

The list is copied from the [Mange/emoji-data][emoji-data] repo.

## License

This plugin is released under the MIT license.

[emoji-data]: https://github.com/Mange/emoji-data
