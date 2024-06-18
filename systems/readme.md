## Systems

The systems folder contains config files for each star system in your mod. These files are optional.

In `SolarSystem.json` you can see modifications we make to the base game solar system. Specifically, we are positioning our new custom ship logs.

In `xen.NewHorizonsExamples.json` we use the unique name of our mod to ensure our system does not conflict with any other mods. We configure a few specific things about our mod:
- We set the `travelAudio` to a custom audio file we've included with the mod. This changes the music that plays when flying between planets.
- We enabled `canEnterViaWarpDrive`. New Horizons adds a warp drive mechanic which allows multiple mods to be installed at once, and you use your ship log to target which system to explore next. For some mods you might not want the warp drive to function, and instead include your own custom puzzle for entering the new system. In that case, set this to false.
- The `Vessel` object allows us to warp into this system using the vessel trapped in Dark Bramble. We have set `alwaysPresent` to true meaning this vessel will always be found orbiting around our custom planet, "Frigid Pygmy".
- The `Skybox` object replaces the skybox in our system with some custom images we've included.

To set the image used in the ship log to show a new solar system, include a `png` file in this folder with the same name as the system! For example here we have `xen.NewHorizonsExamples.png`