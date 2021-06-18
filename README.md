# FLEP_Reverb_Test

Some time ago Chocolate released a new version of FLEP that practically saved the TRLE scene (I think) by fixing the false positive issues. What it also does though is it adds a new patch that adds reverb on PC. Unfortunately PSX reverb and DirectX reverb work in a completely different way and they have completely different presets, so you cannot use the default presets to get the same behavior.

Because of that I have decided to create new presets for FLEP, that mimic the way reverb works in Tomb Raider on PSX. Tomb Raider 4 uses only one preset out of five available on PSX, that is the "STUDIO B" or "STUDIO MEDIUM" preset. The only thing that seems to be changing is the strength of the preset.

My presets work in a similar fashion. I have picked one preset from DirectX defaults that sound the most similar (STONE ROOM preset) and edited it so its volume is different for each available option in TRLE/TE.
The preset was tested with Tomb Editor, but it should be compatible with TRNG as well.

HOW TO INSTALL:
1. Download newest FLEP and its newest patches:
https://www.tombraiderforums.com/showpost.php?p=8299040&postcount=848
https://www.tombraiderforums.com/showpost.php?p=8300607&postcount=890
2. Put all the files in the folder where your tomb4.exe is and open FLEP.
3. Check "Reverb base" and "Reverb classic mode" options.
4. Click on "Reverb classic mode" and set its values to:
- Preset for outside: 0
- Preset for Small Room: 1
- Preset for Medium Room: 2
- Preset for Large Room: 3
- Preset for Pipe: 4
5. Check "Custom 1", "Custom 2", "Custom 3", "Custom 4" and for each set the values as below:

 patchpreset=Custom 1,1,-1000|-500|0.0|2.31|0.64|-711|0.012|-1700|0.017|100.0|100.0|5000.0
 patchpreset=Custom 2,1,-1000|-500|0.0|2.31|0.64|-711|0.012|-1000|0.017|100.0|100.0|5000.0
 patchpreset=Custom 3,1,-1000|-500|0.0|2.31|0.64|-711|0.012|-400|0.017|100.0|100.0|5000.0
 patchpreset=Custom 4,1,-1000|-500|0.0|2.31|0.64|-711|0.012|400|0.017|100.0|100.0|5000.0
 
(The values are in the same order as in FLEP)

Alternatively you can save your preset, then copy the values straight into your new *.fps file. Then you need to reload your preset so the changes are shown in FLEP.
6. Click on Modify and test the game. If you did everything correctly it should work just fine now.

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
