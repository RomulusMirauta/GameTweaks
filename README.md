
# Game Tweaks Repo

<br>

# Table of Contents
I. Far Cry 3

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

<br>

## Launch Options

\GameTweaks\FarCry3\SSs\LaunchOptions.jpg

`-skipintro -offline -RenderProfile_MaxFPS 165`

Command-line argument

- `-skipintro`
	Skip game intro videos.


- `-offline`
	Removes main menu features that are not available anymore: co-op, multiplayer, Uplay.

[!Note]
> Official multiplayer features were disabled in v1.06.
> Community Revival (2026): As of February 2026, a dedicated community project via the Far Cry Discord has successfully "revived" the multiplayer. This allows players to access Co-op and Versus modes again, often requiring a small patch or specific files to redirect the game to community-hosted services.


- `-RenderProfile_MaxFPS X` 
	Forces the game to render at a maximum of *X* FPS.


- `-uplay_steam_mode`
	*did nothing for me


`X` is the preferred max FPS.

This method helps eliminate micro stuttering - especially with the DX11 executable - though this may be the result of combining with below-mentioned fixes & tweaks as well.

The game can be rendered and displayed at 165+ FPS (tested myself), but the stutters/microstutters would happen more often and would be way more aggressive (165 to 32 FPS, if below-settings are not applied).


This fixed the issue where NPCs shake/twitch randomly.







Tested on

instert pc configuration



<br>

## My Config File


Config file location: `Documents\Far Cry 3\`
File name: `GamerProfile.xml`


My config file: [GamerProfile.xml](GameTweaks\FarCry3\GamerProfile.xml)
Config file in "compatibility mode" (with all the tweaks applied): [[COMPATIBILITY]GamerProfile.xml](GameTweaks\FarCry3\[COMPATIBILITY]GamerProfile.xml)






Purpose: finding the balance - maximizing performance and minimizing stutters/microstutters, while keeping the game visually appealing and preserving its high-paced FPS nature.




VSync can help, but also adds some input lag.





```.xml
	<Post>
		<quality GameDepthOfField="0" CinematicDepthOfField="0" MotionBlur="0" FXAALevel="0" id="ultrahigh" />
	</Post>
```


`id="x"` - the other values are:  `low`, `medium`, `high`, `ultrahigh`
if set to `custom`, the blur will remain visible.



This also removes the blur that appears when driving.
Unfortunately, it will not remove the aiming-down sights blur.




`D3D11MultithreadedRendering="1"` altough makes the game run way faster/feel more like a highpaced-FPS, it has caused a lot of random, frequent crashes. Therefore, I recommend `D3D11MultithreadedRendering="0"`







<br>

## Tools and Tweaks

### Large Address Aware (TechPowerUp)

It seems that, by default, the games only uses 2 GB OF RAM (even if you have 32+ GB) - at least on newer PC configurations.
This causes performance issues, and in my case even *frequent* crashes.
We can force the game to utilize 4 GB of RAM, by following these steps:


Tool that assists in making applications LAA (large address aware). When a 32-bit application is LAA, it can access up to 4 GB on x64 OS (operating systems) + all memory that isn't used by the OS and other applications on x86 - Large Address Aware (TechPowerUp)
https://www.techpowerup.com/forums/threads/large-address-aware.112556/


<br>

### Process Lasso (Bitsum)

It seems that, by default, the games only uses 2 cores (even if your CPU has 24 cores!) - at least on newer PC configurations.
This causes performance issues, and in my case even *frequent* crashes.
We can force the game to utilize 4 cores, by following these steps:

Real-Time CPU Optimization and Automation Software for Windows processes. Think of it as an automated task manager. From tuning algorithms like ProBalance to user-created rules and persistent settings such as CPU affinities and priority classes, it gives you complete control to run processes YOUR way! - Process Lasso
https://bitsum.com/





<br>

### NVIDIA Profile Inspector

Tool used for modifying game profiles inside the internal driver database of the NVIDIA driver. All game profiles are provided by the nvidia driver, but you can add your own profiles for games missing in the driver database. You also have access to hidden and undocumented settings, which are not provided by the drivers control panel - nvidiaProfileInspector
https://github.com/Orbmu2k/nvidiaProfileInspector




Category: Sync and Refresh
Parameter: Vertical Sync

Possible Values:
- Fast Sync
Force off
Force on
Fast Sync
Use the 3D application setting
1/2 Refresh Rate
1/3 Refresh Rate
1/4 Refresh Rate


Tried all values => no major improvements


Tried to find fix for issue - annoying, but not game-breaking: NPCs shake/twitch randomlyk.












[!Note]
> Removing Uplay necessity
> Tried multiple methods - had no joy with any of them.
> Decided to not MOD the game, even if some have fixes as well - at least not this time (maybe on the 1.000th playthrough). Main reason: most MODS affect the core gameplay. 