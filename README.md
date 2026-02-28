# Game Tweaks Repo

<br>

# Table of Contents
I. [Far Cry 3](#i-far-cry-3)

<br>

# I. Far Cry 3

## Links and credits:
- https://store.steampowered.com/app/220240/Far_Cry_3/
- https://www.pcgamingwiki.com/wiki/Far_Cry_3
- https://steamcommunity.com/sharedfiles/filedetails/?id=3151589566
- https://www.reddit.com/r/farcry/comments/1err2t6/far_cry_3_fix_random_crashing_and_other_errors_on/
- https://steamcommunity.com/sharedfiles/filedetails/?id=3348375844
- https://www.reddit.com/r/farcry/comments/2nhmzq/psa_this_seriously_fixed_999_of_my_stuttering/
- https://www.reddit.com/r/farcry/comments/2ncqk0/how_to_get_quality_textures_without_the_stuttering/
- https://www.techpowerup.com/forums/threads/large-address-aware.112556/

<br>

## Launch Options

<!-- \GameTweaks\FarCry3\SSs\LaunchOptions.jpg -->

`-skipintro -offline -RenderProfile_MaxFPS 165`

Command-line argument

- `-skipintro`
	Skip game intro videos.


- `-offline`
	Removes main menu features that are not available anymore: co-op, multiplayer, Uplay.

> [!Note]
> Official multiplayer features were disabled in v1.06.
> Community Revival (2026): As of February 2026, a dedicated community project via the Far Cry Discord has successfully "revived" the multiplayer. This allows players to access Co-op and Versus modes again, often requiring a small patch or specific files to redirect the game to community-hosted services.


- `-RenderProfile_MaxFPS X` 
	Forces the game to render at a maximum of *X* FPS.


This method helps eliminate micro stuttering - especially with the DX11 executable - though this may be the result of combining with below-mentioned fixes & tweaks as well.

The game can be rendered and displayed at 165+ FPS (tested myself), but the stutters/microstutters could happen more often and would be way more aggressive (165 to 32 FPS, if below-settings are not applied and if the system is not able to achieve targeted FPS).

This fixed the issue where NPCs shake/twitch randomly.

<br>

Tested the game tweaks mentioned in this repo on PC configuration with the following specs *(and also finished the game)*:

<table>
  <tr>
    <td align="center"><b>PCGameBenchmark</b></td>
	<td align="center"><b>COMPONENT</b></td>
	<td align="center"><b>SPECS</b></td>
  </tr>
  <tr>
    <td rowspan="9"> 
		<a href="https://www.pcgamebenchmark.com/ratemypc?cpu=intel-core-i9-12900k&memory=32gb&gpu=nvidia-geforce-rtx-3080&platform=windows">
		<!-- <img src="https://cdn.pcgamebenchmark.com/signature/intel-core-i9-12900k/32/nvidia-geforce-rtx-3080/large.png" -->
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


<br>


## My Config File

<!-- \GameTweaks\FarCry3\SSs\.jpg -->

Config file location: `Documents\Far Cry 3\`
File name: `GamerProfile.xml`

My config file: [GamerProfile.xml](./FarCry3/GamerProfile.xml) <br>
Config file in *"compatibility mode"* (only with safe-for-all-systems tweaks applied): [[COMPATIBILITY]GamerProfile.xml](./FarCry3/[COMPATIBILITY]GamerProfile.xml)

Purpose: finding the balance - maximizing performance and minimizing stutters/microstutters, while keeping the game visually appealing and preserving its high-paced FPS nature.

VSync can help, but also adds some input lag.


<br>


Explanations for the most important tweaks:

```.xml
	<Post>
		<quality GameDepthOfField="0" CinematicDepthOfField="0" MotionBlur="0" FXAALevel="0" id="ultrahigh" />
	</Post>
```

Disables post-processing effects separately - Depth of field, FXAA, and motion blur are all combined under the "Post FX" graphics setting.

DepthOfField = the effect that simulates the blurring of objects that are out of focus, based on their distance from the camera. It can enhance the cinematic feel of the game, but it can also cause performance issues and make the game look blurry.

FXAA = Fast Approximate Anti-Aliasing is a post-processing technique used to reduce jagged edges (aliasing) in real-time graphics. It works by analyzing the rendered image and applying a blur to areas where it detects high contrast, which helps to smooth out the edges of objects. However, it can also cause a loss of detail and make the image look softer.

0: Disables the effect entirely, which can improve performance and reduce visual clutter, especially in fast-paced action scenes. However, it may also make the game look less cinematic and immersive.
1: Enables the effect, which can provide a subtle improvement in visual quality, at the cost of performance.

`id="x"` <br>
The values can be: `low`, `medium`, `high`, `veryhigh` or `ultrahigh` (depends on the quality preset you choose in the game settings); if set to `custom`, the blur will remain visible. <br>
This also removes the blur that appears when driving. <br>
Unfortunately, it will not remove the aiming-down sights blur.

<br>

- `SSAOLevel="x"` <br>
SSAO = Screen Space Ambient Occlusion = a shading and rendering technique used to calculate how exposed each point in a scene is to ambient lighting. It adds depth and realism to the scene by simulating the way light interacts with objects, creating soft shadows in crevices and corners where light is occluded.

The values can be: `0`, `1`, `2` or `3` 
0: Disables Ambient Occlusion entirely. This is the only way to fully turn it off when running in DirectX 11 mode, as the in-game settings only allow you to switch between different methods (SSAO, HBAO, HDAO).
1: Sets it to the standard SSAO method (default for current chosen graphics preset).
2: HBAO (Horizon Based Ambient Occlusion) - a more advanced method that provides better visual quality than SSAO, but also has a higher performance cost. It simulates occlusion effects based on the horizon line, resulting in more accurate and detailed shadows.
3: HDAO (High Definition Ambient Occlusion) - the most advanced method, but also the most performance-intensive. It provides the best visual quality by simulating more accurate occlusion effects, but it can significantly impact performance on lower-end hardware.


- `D3D11MultithreadedRendering="x"` <br>
Multi-Threaded Rendering = A setting that allows the game to utilize multiple CPU threads for rendering tasks. This can help improve performance by distributing the workload across multiple cores, especially on systems with high core counts. However, it can also introduce instability and cause crashes on some systems, particularly if the game is not optimized for multithreaded rendering or if there are compatibility issues with certain hardware configurations. <br>
Although it makes the game run way faster/feel more like a highpaced-FPS, it has caused a lot of random, frequent crashes. Therefore, I recommend `D3D11MultithreadedRendering="0"`


- `DisableMip0Loading="x"` <br>
Disables the loading of the highest quality mipmap level (mip0) for textures. This can help improve performance by reducing the amount of memory used for textures, but it may also result in lower visual quality, especially when viewing objects up close. It can be useful for players with lower-end hardware or those looking to maximize performance, but it may not be ideal for those who prioritize visual fidelity.

- `AllowAsynchShaderLoading = "x"` <br>
Enables asynchronous loading of shaders, which can help reduce stuttering and improve performance by allowing the game to load shaders in the background while you play. This can be especially beneficial for players with slower storage devices or those who experience frequent stuttering due to shader loading. However, it may also cause some visual glitches or delays in shader loading, so it may not be ideal for all players.

> [!Note]
> In order to edit the config file, remove the "read-only" attribute from the file properties. <br>
> After editing, set it back to "read-only" to prevent accidental changes and alterations made by the game.


<br>


## Tools and Tweaks

### Large Address Aware (TechPowerUp)

<!-- \GameTweaks\FarCry3\SSs\.jpg -->

It seems that, by default, the games only uses 2 GB OF RAM (even if you have 32+ GB) - at least on newer PC configurations and new Windows versions.
This causes performance issues, and in my case even *frequent* crashes.

Tool that assists in making applications LAA (large address aware). When a 32-bit application is LAA, it can access up to 4 GB on x64 OS (operating systems) + all memory that isn't used by the OS and other applications on x86 - Large Address Aware (TechPowerUp)

We can force the game to utilize 4 GB of RAM, by following these steps.

Basic mode:
1) Open an executable to modify (click on the "..." button to browse). Alternatively, you can drag and drop a file on the gray text box.
2) Check or uncheck the box specifying whether or not you want to make it large address aware.
3) Click on save to commit the changes.

Intermediate and advanced mode (Advanced shown):
1) Add files through the "Add" drop down menu or click on on Add Files. Alternatively, you can drag and drop the files into the list view.
2) Select the files you wish to modify by checking the boxes or using the "Select" drop menu.
3) Either click on "Switch Large Address Aware" (turns true to false and false to true) or select an option from the "With Selected" drop down menu.
4) If you wish to remove files from the list, you may do so in Advanced mode via the "Remove" drop down menu.

Requirements:
.NET Framework 3.5 or newer (get the latest version from Windows Update under optional updates).


<br>


### Process Lasso (Bitsum)

<!-- \GameTweaks\FarCry3\SSs\.jpg -->

It seems that, by default, the games only uses 2 cores (even if your CPU has 24 cores!) - at least on newer PC configurations.
This causes performance issues, and in my case even *frequent* crashes.

Real-Time CPU Optimization and Automation Software for Windows processes. Think of it as an automated task manager. From tuning algorithms like ProBalance to user-created rules and persistent settings such as CPU affinities and priority classes, it gives you complete control to run processes YOUR way! - Process Lasso
https://bitsum.com/


We can force the game to utilize 4 cores, by following these steps:
1. Download, install and open Process Lasso
2. Start Far Cry 3 and alt-tab back to Process Lasso
3. Right-click on Far Cry 3 and select "CPU Affinity" > "Always" > "Select CPU Affinity" 
4. Click on "Clear" and select CPU cores: 1, 3, 5, 7
5. Click on "Save Named Affinity" and click OK


<br>


### NVIDIA Profile Inspector

<!-- \GameTweaks\FarCry3\SSs\.jpg -->

Tool used for modifying game profiles inside the internal driver database of the NVIDIA driver. All game profiles are provided by the nvidia driver, but you can add your own profiles for games missing in the driver database. You also have access to hidden and undocumented settings, which are not provided by the drivers control panel - nvidiaProfileInspector
https://github.com/Orbmu2k/nvidiaProfileInspector

Category: Sync and Refresh
Parameter: Vertical Sync

Possible Values:
- Fast Sync
- Force off
- Force on
- Fast Sync
- Use the 3D application setting
- 1/2 Refresh Rate
- 1/3 Refresh Rate
- 1/4 Refresh Rate


Tried all values => Fast Sync seemed to be the best for me, but I recommend testing all options to see which one works best for your specific setup and preferences.

Interesting info: Fast Sync was not a selectable option in NVIDIA Control Panel, but after setting VSync = Fast Sync in NVIDIA Profile Inspector, the option shown up in the NVIDIA Control Panel as well, as "Fast".

<br>

> [!Note]
> Regarding removing Uplay necessity - tried multiple methods - had no joy with any of them.
> Decided to not MOD the game, even if some have fixes as well - at least not this time (maybe on the 1.000th playthrough). Main reason: most MODS affect the core gameplay. 


<br>


## Other tweaks

### NVIDIA Control Panel

<!-- \GameTweaks\FarCry3\SSs\.jpg -->

- Anisotropic Filtering: 8x

Anisotropic Filtering = a texture filtering technique used in 3D graphics to improve the quality of textures on surfaces that are viewed at oblique angles. It works by sampling multiple texels (texture pixels) and applying a weighted average to produce a smoother and more detailed image, especially for textures that are far away or at steep angles. Setting it to 8x can significantly enhance the visual quality of textures, but it may also have a performance impact on lower-end hardware.

- Antialiasing - Mode: Ehnance the application setting

Antialiasing = a technique used to reduce the jagged edges (aliasing) that can occur in digital images, especially in 3D graphics. It works by smoothing out the edges of objects, making them appear less pixelated and more visually appealing. Setting it to "Enhance the application setting" allows the game to control the level of anti-aliasing based on its own settings, which can help balance visual quality and performance.


- Max Frame Rate: Use global setting (On) = 165 FPS

- Monitor Technology: Use global setting (On) = G-SYNC Compatible

- Power management mode: Use global setting (On) = Prefer maximum performance


- Texture filtering - Anisotropic sample optimization: On

Texture filtering = a technique used to improve the quality of textures when they are viewed at different angles and distances. It helps to reduce blurriness and improve the overall visual quality of textures in 3D graphics. Setting it to "Anisotropic sample optimization: On" can help improve performance by optimizing the way textures are sampled, but it may also result in a slight reduction in visual quality, especially for textures that are viewed at steep angles.


- Texture filtering - Negative LOD bias: Clamp

Negative LOD bias = a setting that controls the level of detail (LOD) bias for textures in 3D graphics. It determines how much the game will favor higher or lower resolution textures when rendering objects at different distances. Setting it to "Clamp" prevents the game from using excessively high-resolution textures that can cause performance issues, while still allowing for some level of detail enhancement. This can help improve performance on lower-end hardware, but it may also result in slightly blurrier textures when viewed up close.


- Vertical sync: Fast *(as mentioned above, initially set in [NVIDIA Profile Inspector](###-NVIDIA-Profile-Inspector))*

Vertical sync = a display option that synchronizes the frame rate of the game with the refresh rate of the monitor to prevent screen tearing. Screen tearing occurs when the graphics card outputs frames at a rate that is not in sync with the monitor's refresh rate, resulting in a disjointed image. Setting VSync to "Fast Sync" allows the game to render at a higher frame rate than the monitor's refresh rate, while still preventing screen tearing. This can help reduce input lag and improve performance, especially on high-refresh-rate monitors. However, it may not be ideal for all players, as it can introduce some visual artifacts and may not work well with certain games or hardware configurations.



<br>



Other tweaks that I have applied to the game, but are not mentioned in this repo, are either not safe for all systems (can cause crashes) or do not have a significant impact on performance and/or visual quality.
