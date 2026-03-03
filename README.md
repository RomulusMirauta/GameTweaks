<div align="center">
    <h1>
        Game Tweaks Repo
    </h1>
    <p>
        <em> 
            This repository is a collection of various tweaks, configuration tips, and tools focused on improving performance, stability, and visual quality for games. The goal is to provide a single reference for settings adjustments, launch options, and third-party utilities that can help players get the most out of their systems while playing older or demanding titles. Contributions and updates for other games are welcome as the collection grows.
        </em>
    </p>
</div>


<br><br>


# Table of Contents
I. &nbsp;&nbsp;&nbsp; [Far Cry 3](#i-far-cry-3) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; I. a. &nbsp; [Links and Credits](#i-a-links-and-credits) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; I. b. &nbsp; [Launch Options](#i-b-launch-options) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; I. c. &nbsp; [Config Files](#i-c-config-files) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; I. d. &nbsp; [Main Tools and Tweaks](#i-d-main-tools-and-tweaks) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - [Large Address Aware (TechPowerUp)](#large-address-aware-techpowerup) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - [Process Lasso (Bitsum)](#process-lasso-bitsum) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - [NVIDIA Profile Inspector](#nvidia-profile-inspector) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; I. e. &nbsp; [Other Tweaks](#i-e-other-tweaks) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - [NVIDIA Control Panel](#nvidia-control-panel) <br>
II. &nbsp;&nbsp; [Burnout Paradise Remastered](#ii-burnout-paradise-remastered) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; II. a. &nbsp; [Links](#ii-a-links) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; II. b. &nbsp; [Tweaks and Mods](#ii-b-tweaks-and-mods) <br>
III. &nbsp; [Mirror's Edge](#iii-mirrors-edge) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; III. a. &nbsp; [Links](#iii-a-links) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; III. b. &nbsp; [Fixes & Workarounds](#iii-b-fixes--workarounds) <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; III. c. &nbsp; [Tweaks](#iii-c-tweaks) <br>


<br><br>


# I. Far Cry 3


## I. a. Links and Credits

### Steam & Steam Community Guides and Discussions
- https://store.steampowered.com/app/220240/Far_Cry_3/
- https://steamcommunity.com/sharedfiles/filedetails/?id=3151589566
- https://steamcommunity.com/sharedfiles/filedetails/?id=3348375844


### PCGamingWiki
- https://www.pcgamingwiki.com/wiki/Far_Cry_3


### Reddit
- https://www.reddit.com/r/farcry/comments/2nhmzq/psa_this_seriously_fixed_999_of_my_stuttering/
- https://www.reddit.com/r/farcry/comments/2ncqk0/how_to_get_quality_textures_without_the_stuttering/
- https://www.reddit.com/r/farcry/comments/1err2t6/far_cry_3_fix_random_crashing_and_other_errors_on/


### GitHub
- https://github.com/Orbmu2k/nvidiaProfileInspector


### Microsoft
- https://learn.microsoft.com/en-us/windows-hardware/get-started/adk-install


### CoderBag
- https://www.coderbag.com/Programming-C/Disable-CPU-Core-Parking-Utility


### Bitsum
- https://bitsum.com/


### TechPowerUp
- https://www.techpowerup.com/forums/threads/large-address-aware.112556/


<br><br>


## I. b. Launch Options

```.launchoptions
-skipintro -offline -RenderProfile_MaxFPS 165
```

<br>

![Media](/FarCry3/media/SteamLaunchOptions(2).gif)
<br><br>

Command-line arguments:

- `-skipintro` <br>
  Skips game intro videos. <br><br>

- `-offline` <br>
  Removes main menu features that are not available anymore: co-op, multiplayer, Uplay. <br>

> [!Note]
> - Official multiplayer features were disabled in v1.06. <br>
> - Community Revival (2026): As of February 2026, a dedicated community project via the Far Cry Discord has successfully "revived" the multiplayer. This allows players to access Co-op and Versus modes again, often requiring a small patch or specific files to redirect the game to community-hosted services.

<br>

- `-RenderProfile_MaxFPS X` <br>
  Forces the game to render at a maximum of ***X*** FPS.

> [!Note]
> - This method helps eliminate micro stuttering - especially with the DX11 executable - though this may be the result of combining with below-mentioned fixes & tweaks as well.
> - The game can be rendered and displayed at 165+ FPS (tested myself), but the stutters/microstutters could happen more often and would be way more aggressive (165 to 32 FPS, if below-settings are not applied and if the system is not able to achieve targeted FPS).
> - This fixed the issue where NPCs shake/twitch randomly.

<br><br>

#### Tested the game tweaks mentioned in this repo on `W11 v25H2` and PC configuration with the following specs *(and also finished the game, again)*:

<table>
  <tr>
    <td align="center"><b>PCGameBenchmark</b></td>
	<td align="center"><b>COMPONENT</b></td>
	<td align="center"><b>SPECS</b></td>
  </tr>
  <tr>
    <td rowspan="9"> 
		<img src="https://www.pcgamebenchmark.com/signature/intel-core-i9-12900k/32gb/nvidia-geforce-rtx-3080/twitch.png" 
			alt="PCGameBenchmark" style="width: auto; height: auto; max-width: 100%; max-height: 100%;" />
		</a>
	</td>
    <td align="left"><b>CPU</b></td>
    <td align="left">Intel Core i9-12900K, AL, 16 Cores (8P + 8E), 24 Threads</td>
  </tr>
  <tr>
    <td align="left"><b>GPU</b></td>
    <td align="left">MSI NVIDIA GeForce RTX 3080 GAMING Z TRIO LHR 12GB</td>
  </tr>
  <tr>
	<td align="left"><b>CPU Cooler</b></td>
    <td align="left">Corsair iCUE H150i RGB ELITE 360mm AIO Liquid</td>
  </tr>
  <tr>
	<td align="left"><b>RAM</b></td>
    <td align="left"><b><i>2x</b></i> Kingston FURY Renegade 16GB DDR5 6000MHz D-C Kit</td>
  </tr>
  <tr>
	<td align="left"><b>Motherboard</b></td>
    <td align="left"> GIGABYTE Z690 AORUS ELITE AX</td>
  </tr>
  <tr>
	<td align="left"><b>Storage</b></td>
    <td align="left"><b><i>2x</b></i> SSD Samsung 980 PRO 1TB NVMe PCI-E 4.0 M.2 2280</td>
  </tr>
  <tr>
	<td align="left"><b>Power Supply</b></td>
    <td align="left">Thermaltake Toughpower GF, 80+ Gold, 850W</td>
  </tr>
  <tr>
	<td align="left"><b>Case</b></td>
    <td align="left">Corsair iCUE 4000X RGB Tempered Glass Black</td>
  </tr>
  <tr>
	<td align="left"><b>Monitors</b></td>
    <td align="left"><b><i>2x</b></i> Benq EX2510S MOBIUZ, 24.5" <i>(NVIDIA G-SYNC Compatible)</i></td>
  </tr>
</table>


<br><br>


## I. c. Config Files

![Media](/FarCry3/media/VSCode(2).png)
<br><br>

Config file location: <br>
`%USERPROFILE%\Documents\Far Cry 3` <br>

File name: <br>
`GamerProfile.xml`<br><br>


You can download the config files from here: <br>
- My config file: <br>
  [GamerProfile.xml](./FarCry3/GamerProfile.xml) <br>
- Config file in *"compatibility mode"* (only with safe-for-all-systems tweaks applied): <br>
  [[COMPATIBILITY]GamerProfile.xml](./FarCry3/[COMPATIBILITY]GamerProfile.xml)<br><br>

Purpose: finding the balance - maximizing performance and minimizing stutters/microstutters, while keeping the game visually appealing and preserving its high-paced FPS nature.

<br>

> [!TIP]
> VSync can help, but also adds some input lag.


<br><br>


Explanations for the most important tweaks:

- added lines to the config file *(which are not present in the default one)*

  ```.xml
  <Post>
    <quality GameDepthOfField="0" CinematicDepthOfField="0" MotionBlur="0" FXAALevel="0" id="ultrahigh" />
  </Post>
  ```

  - Disables post-processing effects separately - Depth of field, FXAA, and motion blur are all combined under the "Post FX" graphics setting.

  - `DepthOfField`<br>
  DOF is the effect that simulates the blurring of objects that are out of focus, based on their distance from the camera. It can enhance the cinematic feel of the game, but it can also cause performance issues and make the game look blurry.

  - `FXAA`<br>
  Fast Approximate Anti-Aliasing is a post-processing technique used to reduce jagged edges (aliasing) in real-time graphics. It works by analyzing the rendered image and applying a blur to areas where it detects high contrast, which helps to smooth out the edges of objects. However, it can also cause a loss of detail and make the image look softer.

  - `0`<br>
  Disables the effect entirely, which can improve performance and reduce visual clutter, especially in fast-paced action scenes. However, it may also make the game look less cinematic and immersive.

  - `1`<br>
  Enables the effect, which can provide a subtle improvement in visual quality, at the cost of performance.

  - `id="x"` <br>
  The values can be: `low`, `medium`, `high`, `veryhigh` or `ultrahigh` (depends on the quality preset you choose in the game settings); if set to `custom`, the blur will remain visible. <br><br>
  
  
> [!Note]
> This also removes the blur that appears when driving. <br>
> Unfortunately, it will not remove the aiming-down sights blur.


<br><br>

- `SSAOLevel="x"` <br><br>
SSAO = Screen Space Ambient Occlusion = a shading and rendering technique used to calculate how exposed each point in a scene is to ambient lighting. It adds depth and realism to the scene by simulating the way light interacts with objects, creating soft shadows in crevices and corners where light is occluded. <br><br>
The values can be: `0`, `1`, `2` or `3`. <br>
  - `0`: Disables Ambient Occlusion entirely. This is the only way to fully turn it off when running in DirectX 11 mode, as the in-game settings only allow you to switch between different methods (SSAO, HBAO, HDAO). <br>
  - `1`: Sets it to the standard SSAO method (default for current chosen graphics preset). <br>
  - `2`: HBAO (Horizon Based Ambient Occlusion) - a more advanced method that provides better visual quality than SSAO, but also has a higher performance cost. It simulates occlusion effects based on the horizon line, resulting in more accurate and detailed shadows. <br>
  - `3`: HDAO (High Definition Ambient Occlusion) - the most advanced method, but also the most performance-intensive. It provides the best visual quality by simulating more accurate occlusion effects, but it can significantly impact performance on lower-end hardware. <br><br><br>


- `D3D11MultithreadedRendering="x"` <br><br>
Multi-Threaded Rendering = A setting that allows the game to utilize multiple CPU threads for rendering tasks. This can help improve performance by distributing the workload across multiple cores, especially on systems with high core counts. <br><br>
However, it can also introduce instability and cause crashes on some systems, particularly if the game is not optimized for multithreaded rendering or if there are compatibility issues with certain hardware configurations. <br><br>
Although it makes the game run way faster/feel more like a highpaced-FPS, it has caused a lot of random, frequent crashes. Therefore, I recommend `D3D11MultithreadedRendering="0"`<br><br><br>


- `DisableMip0Loading="x"` <br><br>
Disables the loading of the highest quality mipmap level (mip0) for textures. This can help improve performance by reducing the amount of memory used for textures, but it may also result in lower visual quality, especially when viewing objects up close. <br><br>
It can be useful for players with lower-end hardware or those looking to maximize performance, but it may not be ideal for those who prioritize visual fidelity.<br><br><br>

- `AllowAsynchShaderLoading = "x"` <br><br>
Enables asynchronous loading of shaders, which can help reduce stuttering and improve performance by allowing the game to load shaders in the background while you play. <br><br>
This can be especially beneficial for players with slower storage devices or those who experience frequent stuttering due to shader loading. However, it may also cause some visual glitches or delays in shader loading, so it may not be ideal for all players.<br><br><br>

> [!Note]
> In order to edit the config file, remove the "read-only" attribute from the file properties. <br>
> After editing, set it back to "read-only" to prevent accidental changes and alterations made by the game.


<br><br>


## I. d. Main Tools and Tweaks

### Large Address Aware (TechPowerUp)

![Media](/FarCry3/media/LargeAddressAware(4).gif)
<br><br>

It seems that, by default, the games only uses 2 GB OF RAM ***(even if you have 32+ GB)*** - at least on newer PC configurations and new Windows versions.
This causes performance issues and, in my case, even *frequent* crashes.

There is a tool that assists in making applications LAA (large address aware). When a 32-bit application is LAA, it can access up to 4 GB on x64 OS (operating systems) + all memory that isn't used by the OS and other applications on x86.

<br>

You can download the tool from [here](https://www.techpowerup.com/forums/attachments/laa_2_0_4-zip.34392/).

<br>

We can force the game to utilize 4 GB of RAM, by following these steps.

<br>

Basic mode:
1) Open an executable to modify (click on the "..." button to browse). Alternatively, you can drag and drop a file on the gray text box.
2) Check or uncheck the box specifying whether or not you want to make it large address aware.
3) Click on save to commit the changes.

<br>

Intermediate and advanced mode (Advanced shown):
1) Add files through the "Add" drop down menu or click on on Add Files. Alternatively, you can drag and drop the files into the list view.
2) Select the files you wish to modify by checking the boxes or using the "Select" drop menu.
3) Either click on "Switch Large Address Aware" (turns true to false and false to true) or select an option from the "With Selected" drop down menu.
4) If you wish to remove files from the list, you may do so in Advanced mode via the "Remove" drop down menu.

<br>

Requirements:
.NET Framework 3.5 or newer *(get the latest version from Windows Update under optional updates)*.


<br><br>


### Process Lasso (Bitsum)

![Media](/FarCry3/media/ProcessLasso(1).gif)
<br><br>

It seems that, by default, the games only uses 2 cores (even if your CPU has 24 cores!) - at least on newer PC configurations.
This causes performance issues, and in my case even *frequent* crashes.

Real-Time CPU Optimization and Automation Software for Windows processes. Think of it as an automated task manager. From tuning algorithms like ProBalance to user-created rules and persistent settings such as CPU affinities and priority classes, it gives you complete control to run processes YOUR way!

<br>

You can download the tool from [here](https://dl.bitsum.com/files/processlassosetup64.exe).

<br>

We can force the game to utilize 4 cores, by following these steps:
1. Download, install and open Process Lasso
2. Start Far Cry 3 and alt-tab back to Process Lasso
3. Right-click on Far Cry 3 and select "CPU Affinity" > "Always" > "Select CPU Affinity" 
4. Click on "Clear" and select CPU cores: 1, 3, 5, 7
5. Click on "Save Named Affinity" and click OK


<br><br>


### NVIDIA Profile Inspector

![Media](/FarCry3/media/NVIDIAProfileInspector(1).png)
<br><br>

This tool is used for modifying game profiles inside the internal driver database of the NVIDIA driver. All game profiles are provided by the nvidia driver, but you can add your own profiles for games missing in the driver database. You also have access to hidden and undocumented settings, which are not provided by the drivers control panel.

<br>

You can download the tool from [here](https://github.com/Orbmu2k/nvidiaProfileInspector/releases).

<br>

Category: Sync and Refresh <br>
Parameter: Vertical Sync

<br>

Possible Values:
- Fast Sync
- Force off
- Force on
- Fast Sync
- Use the 3D application setting
- 1/2 Refresh Rate
- 1/3 Refresh Rate
- 1/4 Refresh Rate

<br>

Tried all values => Fast Sync seemed to be the best for me, but I recommend testing all options to see which one works best for your specific setup and preferences.

Interesting info: Fast Sync was not a selectable option in NVIDIA Control Panel, but after setting VSync = Fast Sync in NVIDIA Profile Inspector, the option shown up in the NVIDIA Control Panel as well, as "Fast".

<br>

> [!Note]
> - Regarding removing Uplay necessity - tried multiple methods - had no joy with any of them. <br>
> - Decided to not MOD the game, even if some have fixes as well - at least not this time (maybe on the 1.000th playthrough). Main reason: most MODS affect the core gameplay. 


<br><br>


## I. e. Other Tweaks

### NVIDIA Control Panel

![Media](/FarCry3/media/NVIDIAControlPanel(3).gif)
<br><br>

- Anisotropic Filtering: 8x <br><br>
Anisotropic filtering is a texture filtering technique used in 3D graphics to improve the quality of textures on surfaces that are viewed at oblique angles. <br><br>
It works by sampling multiple texels (texture pixels) and applying a weighted average to produce a smoother and more detailed image, especially for textures that are far away or at steep angles. <br><br>
Setting it to 8x can significantly enhance the visual quality of textures, but it may also have a performance impact on lower-end hardware. <br><br><br>

- Antialiasing - Mode: Ehnance the application setting<br><br>
Antialiasing is a technique used to reduce the jagged edges (aliasing) that can occur in digital images, especially in 3D graphics. <br><br>
It works by smoothing out the edges of objects, making them appear less pixelated and more visually appealing. <br><br>
Setting it to "Enhance the application setting" allows the game to control the level of anti-aliasing based on its own settings, which can help balance visual quality and performance. <br><br><br>


- Max Frame Rate: Use global setting (On) = 165 FPS <br><br>
Max Frame Rate is a setting that allows you to limit the maximum number of frames per second (FPS) that a game can render. <br><br>
Setting it to "Use global setting (On)" allows you to specify a global frame rate limit for all games, which can help reduce screen tearing and improve performance on systems that may struggle to maintain a consistent frame rate. <br><br>
In this case, setting it to 165 FPS *(matching my monitor's max refresh rate)*, can help ensure that the game runs smoothly and reduces the chances of stuttering or micro stuttering, especially on high-refresh-rate monitors. <br><br><br>

- Monitor Technology: Use global setting (On) = G-SYNC Compatible <br><br>
Monitor Technology is a setting that allows you to specify the type of adaptive sync technology that your monitor supports. <br><br>
Setting it to "Use global setting (On)" allows the game to automatically detect and utilize the appropriate adaptive sync technology based on your monitor's capabilities. <br><br>
In this case, setting it to "G-SYNC Compatible" can help reduce screen tearing and improve overall visual quality by synchronizing the game's frame rate with the monitor's refresh rate, especially if you have a G-SYNC compatible monitor. <br><br><br>

- Power management mode: Use global setting (On) = Prefer maximum performance <br><br>
Power management mode is a setting that allows you to specify how the graphics card manages its power consumption. <br><br>
Setting it to "Use global setting (On)" allows the game to utilize the global power management settings specified in the NVIDIA Control Panel. <br><br>
In this case, setting it to "Prefer maximum performance" can help ensure that the graphics card runs at its maximum performance level while playing the game, which can help improve frame rates and reduce stuttering, especially on systems that may struggle to maintain a consistent frame rate. <br><br>
However, it may also result in increased power consumption and heat generation, so it may not be ideal for all players or hardware configurations. <br><br><br>

- Texture filtering - Anisotropic sample optimization: On<br><br>
Texture filtering is a technique used to improve the quality of textures when they are viewed at different angles and distances. <br><br>
It helps to reduce blurriness and improve the overall visual quality of textures in 3D graphics. <br><br>
Setting it to "Anisotropic sample optimization: On" can help improve performance by optimizing the way textures are sampled, but it may also result in a slight reduction in visual quality, especially for textures that are viewed at steep angles. <br><br><br>

- Texture filtering - Negative LOD bias: Clamp<br><br>
Negative LOD bias is a setting that controls the level of detail (LOD) bias for textures in 3D graphics. <br><br>
It determines how much the game will favor higher or lower resolution textures when rendering objects at different distances. <br><br>
Setting it to "Clamp" prevents the game from using excessively high-resolution textures that can cause performance issues, while still allowing for some level of detail enhancement. <br><br>
This can help improve performance on lower-end hardware, but it may also result in slightly blurrier textures when viewed up close. <br><br><br>

- Vertical Sync: Fast *(as mentioned above, initially set in [NVIDIA Profile Inspector](#nvidia-profile-inspector))*<br><br>
Vertical Sync is a display option that synchronizes the frame rate of the game with the refresh rate of the monitor to prevent screen tearing. <br><br>
Screen tearing occurs when the graphics card outputs frames at a rate that is not in sync with the monitor's refresh rate, resulting in a disjointed image. <br><br>
Setting VSync to "Fast Sync" allows the game to render at a higher frame rate than the monitor's refresh rate, while still preventing screen tearing. This can help reduce input lag and improve performance, especially on high-refresh-rate monitors. <br><br>
However, it may not be ideal for all players, as it can introduce some visual artifacts and may not work well with certain games or hardware configurations. <br><br><br>


>[!Note]
> Other tweaks that I have applied to the game, but are not mentioned in this repo, are either not safe for all systems (can cause crashes) or do not have a significant impact on performance and/or visual quality.



<br><br><br>



# II. Burnout Paradise Remastered

## II. a. Links

- https://store.steampowered.com/app/1238080/Burnout_Paradise_Remastered/
- https://www.pcgamingwiki.com/wiki/Burnout_Paradise_Remastered

<br>

Centralized repository of INFO, MODS, PATCHES and TOOLS for the game Burnout Paradise Remastered (PC version): <br>
https://github.com/RomulusMirauta/Burnout-Paradise-Remastered

<br>

## II. b. Tweaks and Mods

Tested the game tweaks and mods mentioned in this repo on `W11 v25H2` and [this PC configuration](#tested-the-game-tweaks-mentioned-in-this-repo-on-w11-v25h2-and-pc-configuration-with-the-following-specs-and-also-finished-the-game-again).

<br>

The tweaks and mods that made my game experience way better, and that I highly recommend:
- Steam Launch Options: 

  ```.launchoptions
  -skipvideos
  ```

- MODs / Patches:
  - [orimarc's BPR Speed Patch](https://community.pcgamingwiki.com/files/file/2058-bpr-speed-patch/)
  - [Bo Anderson's (Bo98) BPR Modder](https://bpr.bo98.uk/)
    - Core Bugfixes (v0.2.1)
    - Traffic Toggle (v1.0)

- Tweaks:
  - [Large Address Aware (TechPowerUp)](#large-address-aware-techpowerup) <br>
  - [Process Lasso (Bitsum)](#process-lasso-bitsum) <br>
  - [NVIDIA Profile Inspector](#nvidia-profile-inspector) <br>

<br>

> [!IMPORTANT]
> These tweaks and mods also helped stabilizing the game, meaning that random crashes are not happening anymore (even in long-play sessions).



<br><br><br>



# III. Mirror's Edge

## III. a. Links
- https://store.steampowered.com/app/17410/Mirrors_Edge/
- https://www.pcgamingwiki.com/wiki/Mirror%27s_Edge

<br>

## III. b. Fixes & Workarounds

If the game crashes on first launch:
1. Go to the game installation folder (e.g., `C:\Program Files (x86)\Steam\steamapps\common\mirrors edge\`) and open the `PhysX` folder
2. Install `PhysX_SystemSoftware.exe`
3. Start the game from Steam

<br>

## III. c. Tweaks
Tested the game tweaks mentioned in this repo on `W11 v25H2` and [this PC configuration](#tested-the-game-tweaks-mentioned-in-this-repo-on-w11-v25h2-and-pc-configuration-with-the-following-specs-and-also-finished-the-game-again).

The tweaks and mods that made my experience with the game way better, and that I recommend to everyone are:
- Steam Launch Options: 

  ```.launchoptions
  -nostartupmovies
  ```

- [Process Lasso (Bitsum)](#process-lasso-bitsum) <br>
- [Large Address Aware (TechPowerUp)](#large-address-aware-techpowerup) <br>

<br>

> [!NOTE]
> These tweaks increased the high-paced feel that the game was meant to have.
