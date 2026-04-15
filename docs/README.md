# Sigma-Spy
A complete Remote Spy with an incredible parser that captures incoming and outgoing remotes data with Actor support!

## Socials 💬
- [Sigma Spy Showcase (Youtube)](https://www.youtube.com/watch?v=Q4VrpE1UfHg) 
- [Discord](https://discord.gg/s9ngmUDWgb) 

## Loadstring
```lua
--// Sigma Spy @depso
loadstring(game:HttpGet("https://raw.githubusercontent.com/0xfinder/Sigma-Spy/refs/heads/main/Main.lua"))()
```

## Notices 🔔
- Sigma Spy will have bugs, please report any bugs by opening an [issue](https://github.com/depthso/Sigma-Spy/issues) on Github
- If you gave a suggestion, please post it in the [discussions](https://github.com/depthso/Sigma-Spy/discussions)
- If you have issues with the executor's comm library (get_comm_channel, create_comm_channel), enable `ForceUseCustomComm` in Sigma Spy/Config.lua which is found in your Executor's workspace folder after running
- AWP and Zenith is recommended to use as of 11/06/25

## Features ⚡
These are some of the many features Sigma Spy has
| | |
| ------------ | ------------- |
| **Actors** support | **Keybinds** for toggling options
| **__index** and __namecall support | **Dumping** logs to file
| **Decompile** large scripts | Argument values for log titles
| **Block** remotes from firing | Wide range of supported data types
| **Spoof** return values _(Return spoofs.lua)_ | Logging client recieves _(e.g **OnClientEvent**)_
| Variable compression in the parser | Remote stacking (Known as 'Grouping') _(optional)_
| Mobile devices are supported | Pop-out editors

## Screenshots 🖼️
<table>
	<tr>
		<td>
			<img src="/docs/images/Basic.png">
		</td>
		<td>
			<img src="/docs/images/DecompileConnection.png">
      Pop-out Decompile with Connections viewer
		</td>
	</tr>
  <tr>
    <td>
      <img src="/docs/images/PopoutWindows.png">
      Mulitple Pop-out editors
    </td>
    <td>
      <img src="https://github.com/user-attachments/assets/87d6b97f-320a-4bff-ab16-4bab1b397d07">
      Executor function patches
    </td>
  </tr>
</table>

## Config.lua options ⚙️
<table>
  <tr>
    <th>Name</th>
	<th>Description</th>
  </tr>
  <tr>
    <td><b>ForceUseCustomComm</b></td>
    <td>Forces Sigma Spy to use the built-in comm library. 
	This is automatically used if you executor does not support it</td>
  </tr>
  <tr>
    <td><b>ForceKonstantDecompiler</b></td>
    <td>Forces the decompile option to use Kontant for decompiling scripts. This is enabled automatically if your executor does not support `decompile`</td>
  </tr>
  <tr>
    <td><b>NoFunctionPatching</b></td>
    <td>Disables patches for functions in your executor that may be vulnerable</td>
  </tr>
   <tr>
    <td><b>ReplaceMetaCallFunc</b></td>
    <td>Replaces the meta call function using getrawmetatable instead of using hookmetamethod</td>
  </tr>
   <tr>
    <td><b>NoReceiveHooking</b></td>
    <td>Disables the hooking of callback functions such as .OnClientInvoke</td>
  </tr>
    <tr>
    <td><b>VariableNames</b></td>
    <td>Variable names used by the parser if the generated is not usuable</td>
  </tr>
</table>

## Required functions ⚠️
Sigma spy will prompt you if your executor does not support it.
Your executor must support these functions in order for it to function:
| Required | Optional |
| ------------ | ------------- |
| hookmetamethod | getcustomasset *(Optional for the true ImGui theme)*
| hookfunction | Comm library (get_comm_channel, create_comm_channel) *(Optional)*
| getrawmetatable | 
| setreadonly| 
| File library |
| getconnections |
| newcclosure |


## Libraries used
- [ReGui (Depso)](https://github.com/depthso/Dear-ReGui/tree/main) 
- [Roblox-Parser (Depso)](https://github.com/depthso/Roblox-parser) 
