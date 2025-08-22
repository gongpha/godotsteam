# GodotSteam for Godot Engine 3.x | Community Edition
An ecosystem of tools for [Godot Engine](https://godotengine.org) and [Valve's Steam](https://store.steampowered.com). For the Windows, Linux, and Mac platforms.

Additional Flavors
---
Pre-Compiles | Plug-ins | Server | Examples
--- | --- | --- | ---
[Godot 2.x](https://codeberg.org/godotsteam/godotsteam/tree/godot2) | [GDNative](https://codeberg.org/godotsteam/godotsteam/tree/gdnative) | [Server 3.x](https://codeberg.org/godotsteam/godotsteam-server/tree/godot3) | [Skillet](https://codeberg.org/godotsteam/skillet)
[Godot 3.x](https://codeberg.org/godotsteam/godotsteam/tree/godot3) | [GDExtension](https://codeberg.org/godotsteam/godotsteam/tree/gdextension) | [Server 4.x](https://codeberg.org/godotsteam/godotsteam-server/tree/godot4) | ---
[Godot 4.x](https://codeberg.org/godotsteam/godotsteam/tree/godot4) | --- | [GDNative](https://codeberg.org/godotsteam/godotsteam-server/tree/gdnative) | ---
[MultiplayerPeer](https://codeberg.org/godotsteam/multiplayerpeer)| --- | [GDExtension](https://codeberg.org/godotsteam/godotsteam-server/tree/gdextension) | ---

Documentation
---
[Documentation is available here](https://godotsteam.com).  You can also check out the Search Help section inside Godot Engine.

Feel free to chat with us about GodotSteam or ask for assistance on the [Discord server](https://discord.gg/SJRSq6K).

Donate
---
Pull-requests are the best way to help the project out but you can also donate through [Github Sponsors](https://github.com/sponsors/Gramps) or [LiberaPay](https://liberapay.com/godotsteam/donate)! [You can read more about donor perks here.](https://godotsteam.com/contribute/donations/)  [You can also view all our awesome donors here.](https://godotsteam.com/contribute/donors/)

Current Build
---
You can [download pre-compiled versions of this repo here](https://codeberg.org/godotsteam/godotsteam/releases).

**Version 3.29**
- Added: new functions and enums to SteamRemotePlay
- Added: Steam icon to the class
- Added: Project Settings for Steam, optional app ID, can set embedded callbacks, thanks to ***TriMay***
- Added: missing HTML Surface functions `openDeveloperTools` and `setDPIScalingFactor`
- Added: missing Video class callbacks `broadcast_upload_start` and`broadcast_upload_stop`
- Changed: replaced previous `MouseCursor` enum with new `HTMLMouseCursor` enum
- Changed: updated docs
- Changed: updated to Steamworks SDK 1.62
- Changed: `getNumSubscribedItems` and `getSubscribedItems` now take include_locally_disabled argument
- Changed: `steamInit` now return intended boolean and first argument removed since client syncs stats/achieves at boot
- Changed: added missing is_system_key argument to `key_down` function
- Fixed: various bits in the in-editor docs
- Fixed: `network_messages_session_failed` missing returned properties in bind
- Fixed: `connected_friend_chat_message` having the wrong signal name
- Fixed: wrong signal name for `get_opf_settings_result`
- Removed: `UserRestrictions` enum
- Removed: `SetPersonaName` function and related callback `name_changed`
- Removed: `GetUserRestrictions` function

[You can read more change-logs here](https://godotsteam.com/changelog/godot3/).

Compatibility
---
While rare, sometimes Steamworks SDK updates will break compatilibity with older GodotSteam versions. Any compatability breaks are noted below. Newer API files (dll, so, dylib) _should_ still work for older versions.

Steamworks SDK Version | GodotSteam Version
---|---
1.62 or newer | 4.14 or newer
1.61 | 4.12 to 4.13
1.59 or newer | 3.23 or newer
1.53 to 1.58a | 3.12 to 3.22.4
1.52 or older | 3.11.1 or older

Versions of GodotSteam that have compatibility breaks introduced.

GodotSteam Version | Broken Compatibility
---|---
3.25 | Networking identity system removed, replaced with Steam IDs
3.26 | sendMessages returns an Array
3.27 | setLeaderboardDetailsMax removed
3.29 | getItemDefinitionProperty return a dictionary, html_needs_paint key 'bgra' changed to 'rbga', removed first argument for stat request in steamInit and steamInitEx, steamInit returns intended bool value


Known Issues
---
- When self-compiling, **do not** use MinGW as it will cause crashes.

Quick How-To
---
For complete instructions on how to build the Godot 4.x version of GodotSteam from scratch, [please refer to our documentation's 'How-To Modules' section.](https://godotsteam.com/howto/modules/) It will have the most up-to-date information.

Alternatively, you can just [download the pre-compiled versions in our Releases section](https://codeberg.org/godotsteam/godotsteam/releases) and skip compiling it yourself!

[To start, check out our tutorial on initializing Steam.](https://godotsteam.com/tutorials/initializing/)  There are additional tutorials with more in the works.  You can also [check out additional Godot and Steam related videos, text, additional tools, plug-ins, etc. here.](https://godotsteam.com/tutorials/external/)

License
---
MIT license
