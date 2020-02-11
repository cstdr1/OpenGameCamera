# OpenGameCamera

OpenGameCamera (OGC) is a free, open-source camera tool for Frostbite games. Our aim is to build a cinematic tool with the freedom to allow content creators, modders and PC users to create stunning artwork.

### Discord Server

For communication, support, sharing, and development, join our Discord server [here](https://discord.gg/HZ676Ff)

## Downloads

The latest release build is available to download here: [Public Releases](https://github.com/coltonon/OpenGameCamera/releases).

# Usage Instructions

Install this **C++ redistributable**: [Download](https://aka.ms/vs/16/release/vc_redist.x64.exe).  
(OpenGameCamera will not work without this.)

Download the injector: [Download](https://cdn.discordapp.com/attachments/548738758053330944/640624916323893297/Injector.exe)  
(Your browser or anti-virus may falsely flag this as dangerous. You must allow the file on your PC.)

Inject OpenGameCamera.DLL with the injector.  
(Star Wars: Battlefront II must be running when you inject OpenGameCamera.DLL, and must be done each time you launch the game.)

## Key Bindings

| Action | Key |
| --- | --- |
| **Show/Hide OpenGameCamera** | Home |
| **Enter/Exit camera** | F5 |
| **Ignore input** | F6 |
| **Show/Hide UI** | F7 |
| **Time-freeze** | F8 |
| **Move camera** | WASD |
| **Cam up** | Space |
| **Cam down** | Ctrl |
| **Fast move** | Shift |
| **Slow move** | Alt |
| **Eject mod** | End |

# Building

## Code Structure

| File | Purpose |
| --- | --- |
| **Source.cpp** | The entrypoint of the modification, and where all of the magic happens |
| **MouseManager.hpp** | Management class for hooking the mouse state, allowing the mod to enable/disable the cursor at will |
| **KeyMan.cpp/hpp** | HotKey management.  Also defined here are the default keybindings. |
| **Renderer.hpp** | Code for hooking into the engine's DebugRenderer functions. |
| **Menu.hpp** | Using renderer.hpp, this code allows easily building and displaying menus. |
| **Candy.hpp** | Hooking class.  Allows VTable hooking, and a wrapper for MinHook. |
| **Typedefs.hpp** | Contains typedefs used for our hooks. |
| **sdk.hpp** | The reverse-engineered game classes. |
| **BasicTypes.hpp** | Definitions for things like vectors and matrices.  Serves to replate DirectX. |

## Building guide

The code is designed to be easily built.  You don't even need the DirectX SDK installed.

1. Clone, or [download](https://github.com/coltonon/OpenGameCamera/archive/master.zip) and extract
2. Open `OpenGameCamera` in Visual Studio
3. Build (Ctrl-B)

# Docs

[Here](https://github.com/coltonon/OpenGameCamera/tree/master/Docs) you can find extended documentation, as well as explantions on various concepts.
