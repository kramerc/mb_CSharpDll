# C# MusicBee Plugin Skeleton

This repository contains a C# skeleton project for developing plugins for MusicBee (https://getmusicbee.com/).

The structure and core plugin interfaces are based on the official MusicBee API documentation and example code provided at:

- MusicBee API documentation (https://getmusicbee.com/help/api/)

Please refer to that page for the latest and authoritative reference on:

- Available plugin interfaces
- Callback methods and events
- Data structures and enums
- Supported capabilities and limitations

## Project Overview

This skeleton is intended as a starting point for creating a MusicBee plugin in C#. It typically includes:

- A class implementing the MusicBeePlugin.Plugin interface
- Handling for plugin initialization and shutdown
- Basic examples of working with the MusicBee player and library
- The correct plugin metadata structure for MusicBee to detect and load the DLL

## Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/kramerc/mb_CSharpDll.git
   ```

2. Open the project in Visual Studio (or your preferred C# IDE).

3. Update plugin metadata (name, description, author, version, etc.) in the main plugin class and/or project properties to match your plugin.

4. Implement your custom logic in the provided skeleton methods (e.g., initialization, event handlers, menu commands).

5. Build the project to produce a DLL.

6. Copy the compiled DLL to the MusicBee plugins folder.

   The path depends on how MusicBee was installed:

   - Microsoft Store installation (per-user AppData path):

     ```text
     C:\Users\<YourUserName>\AppData\Local\Packages\50072StevenMayall.MusicBee_kcr266et74avj\LocalCache\Roaming\MusicBee\Plugins
     ```

     Example for user `kramer`:

     ```text
     C:\Users\kramer\AppData\Local\Packages\50072StevenMayall.MusicBee_kcr266et74avj\LocalCache\Roaming\MusicBee\Plugins
     ```

   - Installer from MusicBee website (per-user Roaming profile):

     ```text
     C:\Users\<YourUserName>\AppData\Roaming\MusicBee\Plugins
     ```

     Example for user `kramer`:

     ```text
     C:\Users\kramer\AppData\Roaming\MusicBee\Plugins
     ```

7. Restart MusicBee and enable/configure the plugin via:

   Edit → Preferences → Plugins

## Attribution

This project is derived from and/or closely follows the example code and documentation provided on the official MusicBee API help page:

- https://getmusicbee.com/help/api/

All credit for the API design and original examples goes to the MusicBee developer(s). This repository simply packages that structure into a reusable C# project skeleton.

## License

This repository does not define its own license beyond what is permitted by the original MusicBee API example and documentation. If you intend to distribute derived work, please ensure that you comply with:

- Any terms or conditions presented on https://getmusicbee.com/help/api/
- Any additional licensing information provided with the MusicBee application or documentation

If you add your own code or redistribute this skeleton, you may wish to include an explicit license file (e.g., MIT, Apache-2.0) to cover your contributions.
