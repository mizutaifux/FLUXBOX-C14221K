# FLUXBOX-C14221K
### Fluxbox - simple theme
---
**Wallpaper**: Solid blue color.

**GTK Theme**: Arc (default in distro)

**Icon Theme**: Breeze_light (default in distro)

**Fonts**: Andale Mono (default in distro)

**Other**: Sakura(terminal), Tmux, VIM (editor), GpicView (Image viewer), System Tray (Steam, Fluxbox VWM)

*Nothing special more usual.*


## Preview

![Preview](2025-12-14-093815_1920x1080_scrot.png)


## Create XDG-Menu (custom in menu file)

### Step-by-Step Mini Guide to Create xdg_menu for Fluxbox

Install Required Packages:

Ensure you have the necessary packages. You might need to install xdg-utils and fluxbox. Use your package manager to install these.

Create the Menu File:

You’ll typically define your menu in the ~/.fluxbox/menu file. This will be your main menu configuration.

```bash
nano ~/.fluxbox/menu
```

Add xdg_menu:

Insert the following line in your Fluxbox menu file to call the xdg_menu:

```plaintext
[exec] (Applications) {xdg-menu}
```

Generate the Menu:

If needed, create a shell script to generate the menu dynamically. You can use the following basic script:

```bash
#!/bin/bash
xdg-menu-parse > ~/.fluxbox/menu
```

Make the script executable:

```bash
chmod +x /path/to/your/script.sh
```

Update the Menu:

Run your script whenever you want to update the Fluxbox menu based on changes in the installed applications:

```bash
/path/to/your/script.sh
```

Reload Fluxbox:

After updating your menu, you may need to reload Fluxbox to see the changes. You can do this through the Fluxbox menu by selecting Reload.
