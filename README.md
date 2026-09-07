
<h1 align="center">
TerraAngel
</h1>
<p align="center">
TerraAngel is a modern and feature-rich utility client for Terraria. fork with my own stuff :&nbsp;&nbsp;)
</p>
<br>

## fork changes and plans

- [x] additional editable properties and organization in item editor
- [x] change behavior of giving items from item browser
  - click for only 1, hold shift and click for a full stack. multiple clicks will add to the stack
- [ ] options to control player luck
- [ ] options to control fishing catch quality
- [ ] make your own aliases for chat
- whatever else later on that i feel would be useful (feel free to open an issue for suggestions)

## Installation

Please note that this client is currently only available for Windows and Linux

In order to use it, you will need to have [git](https://git-scm.com/install/), [PowerShell 7](https://learn.microsoft.com/en-us/powershell/scripting/install/install-powershell), [.NET 8 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/8.0) and [.NET 10 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/10.0) installed on your machine

Be sure to restart your computer after you install these

To install the client, follow these steps:

  1. Open Terminal or Command Prompt

  2. Run the following command
  ```bash
  git clone https://github.com/c3omg/TerraAngel.git --recursive
  ```
  3. Run the command `cd TerraAngel`. If you are on **Windows** you can run `./fast.ps1 -Start` and continue on to step 4<br><details><summary>For Linux Users</summary>

      1. Right click Terraria in your Steam library and press "Properties"
      
      2. Click "Compatibility" and enable "Force the use of a specific Steam Play compatibility tool" (Proton version doesn't matter, you just need Steam to download the Windows binary instead)

      3. Once Steam finishes downloading, right click Terraria in your library again. Hover over "Manage" and press "Browse local files"

      4. Copy all the files to `./steam/Terraria` (create the Terraria folder if it doesn't exist)

      5. Run `pwsh`, then run `./fast.ps1 -Download -Start`
      
      > In case you get any errors about a missing dependency, make sure `curl`, `7zip`, `msitools`, and `tar` are installed from your package manager.

  </details>

  4. Wait for it to finish. This may take around 1-3 minutes. Once it completes successfully, the client will be built in `./src/TerraAngel/Terraria/bin/Release/net10.0`

## Updating

Whenether there is a Terraria update, update Terraria on Steam first, then run `./fast.ps1 -Decompile`

(Linux user have to do `./fast.ps1 -UpdateGame -Decompile`)

To update TerraAngel and pull any changes, run `./fast.ps1 -Update`

Then run `./fast.ps1 -Compile` to build the updated client

(Or run `./fast.ps1 -Download -UpdateGame -Decompile -Update -Compile` to do all of these at once)

## Development

After installing the client, you can edit the source code of the client in `src/TerraAngel/Terraria`

Run `./fast.ps1 -Diff` to create patches based on your changes

## Client features

### Features for Terraria developers

- Inspector
    - Inspect player information
    
    ![image](https://user-images.githubusercontent.com/87276335/227608993-092563ba-64f2-4102-9cbe-1c3723bf8e68.png)
    - Inspect NPC information
    
    ![image](https://user-images.githubusercontent.com/87276335/227608567-45571da7-b75a-4057-8fa8-a7501bcad51f.png)
    - Inspect projectile information
    
    ![image](https://user-images.githubusercontent.com/87276335/227608900-8a275a82-ee30-4352-b692-8d929bc270bf.png)
    - Inspect item information
    
    ![image](https://user-images.githubusercontent.com/87276335/227608459-e5c5bd79-1684-419b-84dd-a5d898b5e3c6.png)
    
- Freecam: allows you to move the camera freely around the game world
- Visual utilities: a range of tools to help visualize various aspects of the game
   - View player hitboxes
   - View player held items
   - View player inventories
   - View NPC hitboxes and visualize NPC lag
   - View projectile hitboxes
   - View tile section borders
   - Disable dust
   - Disable gore
   - Show detailed item tooltips

   ![image](https://user-images.githubusercontent.com/87276335/197304559-292de6a7-bed1-4cc9-a452-89d70e890981.png)
- Interactive C# execution engine (aka [REPL](https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop))
  - Real time auto-completion
- Net message debugger
  - Logging send and received
  - Stack traces of packets that are sent
  - Send messages with custom values and generate NetMessage.SendData calls
- Disable tile framing
- Supports any CPU (x64 and x86)
- See [PLUGINS.md](/PLUGINS.md) for information about plugins

### Other useful features

- Complete re-write of the chat UI
![Terraria_1660961693](https://user-images.githubusercontent.com/87276335/185725363-591a1d7b-a264-4a46-bfb2-96578c8ad6a3.gif)
- Complete re-write of the multiplayer server UI
- Anti-Hurt/Godmode
- Fullbright
- Noclip
- Item browser
- Revealing the map
- Infinite reach, mana, and minions
- Access to journey UI
- Butchering NPCs
- Projectile prediction
- Customizable UI
- World edit 
  - Tile brush
    - Basic tile manipulation
    - Basic liquid manipluation
  - Copy-pasting parts of the world
- Re-write of how the game stores tiles (game uses 500mb less memory)
- Viewing other players inventories
- Direct screenshots of the map
- Many bugfixes
- Some minor optimizations and performance improvements
- Ability to change FPS cap

## Planned features

- Some epic optimizations
- UHHHHHHHH

## System Requirements

Because TerraAngel uses FNA instead of XNA, not all devices are compatible

- Windows 7+
- OpenGL 3.0+ or D3D11

## How to Contribute

  1. Fork the repository to your own GitHub account.
  2. Make the desired changes in your forked repository.
  3. Open a pull request from your forked repository to the original repository.
  4. The project maintainer will review your pull request and may suggest changes or accept it if it is suitable.

We welcome contributions of all kinds, including code improvements, bug fixes, and new features.

## Questions?

Open an issue
