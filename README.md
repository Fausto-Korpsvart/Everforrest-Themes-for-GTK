<h1 align="center">Everforest GTK Theme</h1>

<p align="center">
  <img alt"Linux Logo" = src="https://img.shields.io/badge/OS-Linux-FCC624?style=for-the-badge&logo=linux&logoColor=yelow"/>
  <img alt"CSS Logo" src="https://img.shields.io/badge/Style-CSS-blue?style=for-the-badge&logo=css3&logoColor=blue"/>
  <img alt"GitHub Stars" src="https://img.shields.io/github/stars/Fausto-Korpsvart/Everforest-GTK-Theme?&style=for-the-badge&logoColor=red" />
  <img alt"GitHub Forks" src="https://img.shields.io/github/forks/Fausto-Korpsvart/Everforest-GTK-Theme?style=for-the-badge" />
  <img alt"GitHub Issues" src="https://img.shields.io/github/issues/Fausto-Korpsvart/Everforest-GTK-Theme?style=for-the-badge" />
  <img alt"GNU License" src='https://img.shields.io/github/license/Fausto-Korpsvart/Everforest-GTK-Theme?style=for-the-badge&logo=GNU&label=License&color=bd0000&logoColor=white'/>
</p>

> [!NOTE]
> Description
> A GTK theme based on the colours of [Sainnhe's](https://github.com/sainnhe) great theme: [Everforest for Neovim](https://github.com/sainnhe/everforest),
> the [VinceLiuice's](https://github.com/vinceliuice) awesome: [Magnetic GTK theme](https://github.com/vinceliuice/Magnetic-gtk-theme)
> and the creativity of [Gusbemacbe's](https://github.com/gusbemacbe): [Suru Plus Icon Theme](https://github.com/gusbemacbe/suru-plus).<br>
>
> The theme is more focused on the Gnome Desktop, but supports Cinnamon, XFCE, Mate, etc. with generic styles.
> It's great to combine in your TWMs like: XmonadWM, AwesomeWM, BSPWM, etc...
>
> You can check **Reddit:** [r/unixporn](https://www.reddit.com/r/unixporn/) to get some ideas.

![Everforest](https://raw.githubusercontent.com/Fausto-Korpsvart/Everforest-GTK-Theme/master/extra/screenshots/Everforest1.png)

## Installing Themes

Before installing, make sure to install the `Murrine Engine` and `gnome-themes-extra` packages for the correct rendering of themes.

Here are some commands to install on some distributions.

- On Fedora run:

```sh
 sudo dnf install gtk-murrine-engine
```

- On OpenSUSE run:

```sh
 sudo zypper install gtk2-engine-murrine
```

- On Arch run:

```sh
sudo pacman -S gtk-engine-murrine
```

- On Debian and derivatives run:

```sh
sudo apt install gtk2-engines-murrine
```

The themes work on versions 40 to 44 of the GNOME D.E. just follow the steps below for installation:

- Download the [themes](https://www.pling.com/u/fkorpsvart) packs and extract them
- Move the extracted files to the following paths:
  - For GTK3: `~/.themes` In this path you must move the entire theme folder.
  - For GTK4: `~/.config/gtk-4.0` The files to move to this path can be found inside the theme directory in the `gtk-4.0` folder,
    copy only the `assets`, `gtk.css` and `gtk-dark.css` files or create a symlinks.

### Applying themes from zip files

- For GTK3, apply themes from **Gnome Tweaks**.
- For GTK4 applications it is only necessary to have moved the `assets`, `gtk.css` and `gtk-dark.css` files to the `~/.config/gtk-4.0` path,
  and if you notice that the theme has not been applied, just close and reopen the application.

### Applying themes to Flatpak applications

- Override flatpak themes to `~/.themes`:

```sh
sudo flatpak override --filesystem=$HOME/.themes
```

- Override flatpak icons to `~/.icons`:

```sh
sudo flatpak override --filesystem=$HOME/.icons
```

- Override flatpak themes to `~/.config/gtk-4.0` locally:

```sh
flatpak override --user --filesystem=xdg-config/gtk-4.0
```

- Override flatpak themes to `~/.config/gtk-4.0` globally:

```sh
sudo flatpak override --filesystem=xdg-config/gtk-4.0
```

**Alternative Flatpak Theming: [stylepak](https://github.com/refi64/stylepak)**

## Script Installation

Run the following command in the terminal for a general installation

```sh
./install.sh
```

The `./install.sh` allows some specific options like:

```sh
./install.sh --tweak moon mac outline float -t green -l
```

> For more information, run: `./install.sh --help`

```
-d, --dest DIR          Specify destination directory (Default: ~/.themes)
-n, --name NAME         Specify theme name (Default: Everforest)
-t, --theme VARIANT...  Specify theme accent color variant(s) [default|purple|pink|red|orange|yellow|green|teal|grey|all] (Default: blue)
-c, --color VARIANT...  Specify color variant(s) [light|dark] (Default: All variants)
-s, --size VARIANT...   Specify size variant [standard|compact] (Default: standard variant)

-l, --libadwaita        Link installed gtk-4.0 theme to config folder for all libadwaita app use this theme

-r, --remove,
-u, --uninstall         Uninstall/Remove installed themes or links

--tweaks                Specify versions for tweaks
                        1. [medium|soft]  Medium|Soft| ColorSchemes version
                        2. black          Blackness color version
                        3. float          Floating gnome-shell panel style
                        4. outline        Windows with 2px outline style

-h, --help              Show help
```

### Clarifying some doubts

This is just to clarify doubts about the abbreviations of the Themes, as many found the names confusing.

| Abbreviation example | Explanation of abbreviations                                   |
| -------------------- | -------------------------------------------------------------- |
| Theme-Name-B-MB      | Theme with `Border` decoration and `macOS Buttons` in windows  |
| Theme-Name-B-LB      | Theme with `Border` decoration and `Legacy Buttons` in windows |
| Theme-Name-B-GS      | Theme with `Border` decoration for `Gnome Shell`               |
| Theme-Name-BL-MB     | Theme `Borderless` decoration and `macOS Buttons` in windows   |
| Theme-Name-BL-LB     | Theme `Borderless` decoration and `Legacy Buttons` in windows  |
| Theme-Name-BL-GS     | Theme `Borderless` decoration for `Gnome Shell`                |

### Looking for other themes with Neovim colour schemes?

| Neovim Colorschemes for GTK   | GitHub                                                              | Pling                                       |
| ----------------------------- | ------------------------------------------------------------------- | ------------------------------------------- |
| Catppuccin GTK Theme          | [Source](https://github.com/Fausto-Korpsvart/Catppuccin-GTK-Theme)  | [Package](https://www.pling.com/p/1715554/) |
| Everforest GTK Theme          | [Source](https://github.com/Fausto-Korpsvart/Everforest-GTK-Theme)  | [Package](https://www.pling.com/p/1695467/) |
| Gruvbox GTK Theme             | [Source](https://github.com/Fausto-Korpsvart/Gruvbox-GTK-Theme)     | [Package](https://www.pling.com/p/1681313/) |
| Kanagawa GTK Theme            | [Source](https://github.com/Fausto-Korpsvart/Kanagawa-GKT-Theme)    | [Package](https://www.pling.com/p/1810560/) |
| Material GTK Theme            | [Source](https://github.com/Fausto-Korpsvart/Material-GTK-Themes)   | [Package](https://www.pling.com/p/1706139/) |
| Nightfox GTK Theme            | [Source](https://github.com/Fausto-Korpsvart/Nightfox-GTK-Theme)    | [Package](https://www.pling.com/p/1929101/) |
| Rose Pine GTK Theme           | [Source](https://github.com/Fausto-Korpsvart/Rose-Pine-GTK-Theme)   | [Package](https://www.pling.com/p/1810530/) |
| Tokyonight GTK Theme          | [Source](https://github.com/Fausto-Korpsvart/Tokyonight-GTK-Theme)  | [Package](https://www.pling.com/p/1681315/) |

#### Acknowledgements to

Thanks to [@f1yn](https://github.com/f1yn) for the solution to the active and inactive borders in the new version of `Cinnamon.`

Thanks to [@telometto](https://github.com/telometto) for the alternative to the application of themes in `Flatpak.`

#### Support

[![PayPal Support](https://img.shields.io/badge/Donate-PayPal-00457C?style=for-the-badge&logo=paypalColor=white)](https://www.paypal.com/donate/?hosted_button_id=LKVTXNA36FTV4)
