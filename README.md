# PathofExileFix
## Might fix the shitty stuttering and FPS lags POE1+2 related.

### 1) My Desktop PC:
CPU: AMD Ryzen 7 3800X 8-Core Processor 3.90 GHz

GPU: AMD Radeon RX 6900 XT

RAM: 64GB Corsair Vengeance LPX schwarz DDR4-3200 DIMM CL16 Dual Kit

### 2) About the problem:
Never had any stable performance since Path of Exile 1 long ago. Always made some PC upgrades from time to time, and yet other games ran perfect, just POE never did. Friends encountered similar problems. The most annoying was definitive all the micro stuttering, you just recognize when playing.

First starting with standalone client gave the absolute worst performance. Nearly unplayable. Then switching to Steam made it somehow a bit better, no idea why. But was far away from perfect.

Then you think POE 2 will make things better? No, absolutely not. Yes it looks better, but runs exactly the same performance wise. I've read POE 2 is a fork from a specific POE 1 version (don't remember).

I remembered someone very long time ago in the forums, talking about sound bringing down performance a lot in this game. Also when the game is loading stuff in the background, FPS goes down to kinda 0. So I tried out a few startup parameters on Steam. And guess what, I can finally play Path of Exile on nearly stable FPS.

Here's my results, and actually I can play the game:

#### FPS before
min. 30 to max. 60 FPS
#### FPS after
min. 50 to max. 95 FPS

### 3) My Graphic Settings:

Will run better with NVIDIA DLSS, but going FSR with AMD gives pretty good results too. A lot better than the setting NIS (default). Monitor ofc is set to 144 Hz. You could try go up on the Detail Settings but for me I'm fine this way.

##### Display Settings
* Renderer: Vulkan
* Mode: Windowed Fullscreen (Yes fullscreen might get more FPS, but no Overlays possible then)
* VSync: Adaptive
* Resolution: Your Width x Height
* Upscale Mode: FSR
* Max Image Quality: No Upascale (Native AA)
* Sharpness: 100%

##### Detail Settings
* Texture Quality: Medium
* Texture Filtering: 2x Anisotropic Fitlering
* Lighting: Shadows
* Shadow Quality: Low (Default)
* Sun Shadow Quality: Low
* Number of Lights: Low
* Bloom: 25%
* Water Detail Level: Low

##### Advanced Settings
* NVIDIA Reflex: Off
* Triple-Buffering: On
* Dynamic Culling: On
* Target Framerate: 120
* Engine Multithreading: On

### 4) On Steam I am on these start commands now:

**-USEALLAVAILABLECORES --nologo --waitforpreload --noasync --softwareaudio**

I added parameteres one after another, then testing, then adding the next. What really made it for me was **--softwareaudio** (lol).

The Available Cores thing should be already covered with the **Engine Multithreading** setting, but still keeping it here. No Logo just a QoL thing. Wait for preloading will prevent background-loaded stuff from what the Wiki says and No Async completely disables asynchronous loading.

*You can read all info about start parameters also here on the wiki, it works on the standalone too: https://pathofexile.fandom.com/wiki/Launch_options*

*I made another quick search on that sound information and found a reddit of 5 years ago, describing pretty much same results on the performance increase on the sound thing, look here:
https://www.reddit.com/r/pathofexile/comments/ei3d1u/performance_tip_you_can_actually_reap_the_nosound/*
