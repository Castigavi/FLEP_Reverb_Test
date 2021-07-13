# FLEP_Reverb_Test

Some time ago Chocolate released a new version of FLEP that practically saved the TRLE scene (I think) by fixing the false positive issues. What it also does though is it adds a new patch that adds reverb on PC. Unfortunately PSX reverb and DirectX reverb work in a completely different way and they have completely different presets, so you cannot use the default presets to get the same behavior.

Because of that I have decided to create new presets for FLEP, that mimic the way reverb works in Tomb Raider on PSX. Tomb Raider 4 uses only one preset out of five available on PSX, that is the "STUDIO B" or "STUDIO MEDIUM" preset. The only thing that seems to be changing is the strength of the preset.

My presets work in a similar fashion. I have picked one preset from DirectX defaults that sound the most similar (STONE ROOM preset) and edited it so its volume is different for each available option in TRLE/TE.
The preset was tested with Tomb Editor, but it should be compatible with TRNG as well.

HOW TO INSTALL:

Easy way (if you don't use other FLEP patches):
1. Go to the top of this page, click on green Code button and click Download Zip option.
2. Copy flep.cfg, flep.dll, flep.exe, FLEP_ReverbX.fps (X being highest number), patches.bin, patches.dat, patches.flp, plugins.parc, preset.fps, tomb4.exe files to your TRLE folder.
3. It should work already. You can still use FLEP to apply additional patches.

Advanced way (if you already use FLEP for other things):
1. Make sure your current FLEP configuration is saved into a preset file.
2. Download newest version of FLEP and newest patches version here: https://www.tombraiderforums.com/showthread.php?t=196854&page=89
3. Download FLEP_ReverbX.fps preset from the repository. Open it in Notepad and find these lines:  
 patchpreset=Sample file size,1,2097152  
 patchpreset=Sample rate,1,22050  
 patchpreset=Sample buffer array,1  
 patchpreset=Reverb base,1  
 patchpreset=Reverb classic mode,1,0|1|2|3|4  
 patchpreset=Reverb advanced mode,0  
 patchpreset=Custom 1,1,-1000|-500|0.0|2.31|0.64|-711|0.012|-1700|0.017|100.0|100.0|5000.0  
 patchpreset=Custom 2,1,-1000|-500|0.0|2.31|0.64|-711|0.012|-1000|0.017|100.0|100.0|5000.0  
 patchpreset=Custom 3,1,-1000|-500|0.0|2.31|0.64|-711|0.012|-400|0.017|100.0|100.0|5000.0  
 patchpreset=Custom 4,1,-1000|-500|0.0|2.31|0.64|-711|0.012|400|0.017|100.0|100.0|5000.0   
Copy them and close the file (values might differ in later versions of FLEP_ReverbX.fps file so always copy them from the file itself, not above).
4. Open your preset file and copy the above values into their corresponding places. Save and close.
5. Before patching MAKE SURE that your patches.bin file is clean (so it wasn't patched before).
5. Patch the game and test.

If after patching the game you have crashes or other issues, please refer to THIS post for troubleshooting.

TROUBLESHOOTING:
1. Make sure patches.bin was not extensively modified before.
 - FLEP inherits patching behaviour from TREP, which is good for simple patches but not so much for complex ones like reverb. According to Chocolate, if your game crashes it is possible that you have messed around with "advanced reverb" mode and then switched to "classic" (and vice versa). This may result in a faulty patches.bin. If that's the case, redownload patches.bin from latest FLEP version (or my repository) and try patching again.
 - You can still use your own presets and apply new ones afterwards. This step is only to make sure that FLEP patches a "clean" patches.bin file.
2. Check your number formats settings in Control Panel. It seems FLEP has issues with decimal symbols (just like Leikkuri) so it may crash if your region format uses comma instead of dot for decimals (eg. 1,23 instead of 1.23).
 - To fix that go to All Settings / Time & Language / Date, time & regional formatting and set 'Regional format' to English (United Kingdom).
 - Alternatively you can instead go to Additional date, time & regional settings / Change date, time or number formats / Additional settings and change 'Decimal symbol' there to dot (you can also go there to check if your decimal symbol really is dot instead of comma).

HOW TO USE IT:
The way the presets work is pretty simple and it mimics the way reverb works on PSX, so:

Small - this option gives a very subtle reverb. It is very hard to hear, especially with ambient music. It should be used in small rooms.  
Medium - This one gives a bit stronger reverb, but it is still rather subtle. It should be used in medium sized rooms.  
Big - This gives a strong and noticeable reverb. The echo is very prominent. It should be used in big rooms only.  
Pipe - This one has the strongest reverb, super loud. It was barely ever used in the original games and it should only be used in really huge rooms I suppose.  

I have also made a short video from one of my WIP custom levels that show what the reverb presets sound like:

Moreover, TheBlueFox has kindly ported a small test level of mine to PSX, so you can play it on PSX/PSX emulator/PSP to compare reverb. Notice that I couldn't reproduce the exact same effect, so it might differ a bit. Big thanks to TheBlueFox for the conversion, without it I wouldn't have even started works on the reverb presets!

PSX Reverb Test Level: https://drive.google.com/file/d/1m3OEA0jGPQZG9wMNZ1ihFhUYeoaPGKvb/view?usp=sharing

https://www.youtube.com/watch?v=PVvPyzMuelE

* - The link redirects to my github page with the project I used to test FLEP reverb. It is possible that in future I might do more changes to those presets. All the changes will be visible on develop branch before merging with master.

P.S. - I know this looks like a tutorial and I even thought about putting it there, BUT this stuff is still WIP, I might still be making changes to it and moreover, I would absolutely love insight from the community how can I perfect the presets. Most threads in tutorial section are closed so that would be impossible. If a mod feels like this stuff belongs somewhere else though feel free to move it. :)

IMPORTANT:
If you are going to use those presets and edit them, please share your results with the community. It will be the easiest and fastest way to correct the presets in order to get them as close to PSX reverb as possible.
