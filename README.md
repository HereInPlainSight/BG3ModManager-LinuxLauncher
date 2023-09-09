# BG3ModManager-LinuxLauncher
### Linux Launcher and non-Steam game adder for [BG3ModManager](https://github.com/LaughingLeader/BG3ModManager)

Run without arguments to launch BG3ModManager. Must first be setup using --setup flag.

**Dependencies:**
 - [BG3ModManager](https://github.com/LaughingLeader/BG3ModManager)
 - Python3
 - wine
 - winetricks
 - Python Packages (for non-Steam game shortcut support):
     - vdf
     - pefile

**Installation:**
 - EXIT STEAM!
 - Put "[linux.py](https://raw.githubusercontent.com/Kuuchuu/BG3ModManager-LinuxLauncher/main/linux.py)" in the same directory as "BG3ModManager.exe"
 - Using a terminal run the python script with the "--setup" flag (optionally include the "--steam" flag)

**Flags:**

 - `--setup`
     - Setup the WINEPREFIX and settings.json.
         - You will need to click through the .NET Framework installers as they pop up:
             - .NET Framework 4.0
             - .NET Framework 4.5
             - .NET Framework 4.6
             - .NET Framework 4.6.1
             - .NET Framework 4.6.2
             - .NET Framework 4.7.2
 - `--steam`
     - Add to Steam as a non-Steam game.
     - **Requires `pip install vdf pefile`**
 - `--clean`
     - Removes the WINEPREFIX. Can be used with --setup for a fresh install.
 - `--debug`
     - Uploads all output to termbin.com with a 1 month expiration date. Provides the URL to the user.
       - Your WINEPREFIX location, script location, and likely username will be in the uploaded output, but the output will not be publicly listed (until you provide it).

All flags can be passed simultaneously.

**Known Issues:**

 - BG3ModManager window may appear black when launched.
     - Dragging the window around should fix the window's rendering.
 - Uploaded debug output currently gets cut off in the middle of the .NET 4.6.1 installation.
     - I'll have the script clean up the debug output before uploading (removing repeating fixmes)
