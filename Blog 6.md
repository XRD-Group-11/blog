# Blog 6

## Requirements Completed

During this period, we managed to add:

- **Shooting Mechanics (Recoil)**

  - The shooting was handled by listening to the `XRGrabIntractable` events, when the select button is pressed we fire a raycast so we can spawn a hit particle, play the muzzle particle system and play the ak-47 shoot sound. The recoil is handled by having a clamped value that ranges between 0 and 1 and it increase while shooting and decreases when not shooting. This value will determine how much will the bullet go of the main shooting trajectory. The first bullet always lands where we aim. We are also simulating a bullet in the chamber, after all of the bullets have been emptied from the magazine there is still one bullet left in the chamber, or by having a bullet in the chamber and adding a full magazine of 30 bullets, we have now 31 bullets at our disposal.

- **Movement**

  - Movement was slightly tweaked to be more natural and fitting for our game needs.

- **Grenades (HE Grenade)**

  - Explosion particles were added using the Unity Asset Store, then made into a prefab for a grenade.
  - Sound was implemented by adding a sound to the Audio Manager and calling it in the Grenade script; when the grenade explodes, the sound is played.
  - A model and texture were added for the grenade with the ability to be grabbed.

- **Textured Models**

- **Reload Mechanic (Almost Completed)** -

      	- The player can take out the magazine and put it back in. Each magazine has its own ammo capacity. Full reloading is done by taking out the magazine, taking a new full magazine, putting it back in to the gun and then cooking the bolt. The cooking of the bolt is still not working 100%, we need to make the bolt intractable and make it slide back while still being attached to the gun model.

- **Sounds**

  - Some sounds have been added for shooting and grenade explosions.
  - Sounds were brought from the official CS 1.6 game, with missing sounds sourced from the internet.
  - The Audio Manager was implemented to manage all the sounds.

- **Particles**

  - Particles for explosions, muzzle flashes, and bullets hitting were added.
  - All of the particles were sourced from the Unity Asset Store and integrated into the game to serve their respective purposes (e.g., muzzle flash when the AK shoots).

- **Skybox**
  - A skybox was added through the Unity Asset Store.
