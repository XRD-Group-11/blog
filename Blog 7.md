# Blog 7

## Requirements Completed

During this period, we managed to add:

## Charging handle

We have tried using built-in unity physics, in particular `ConfigurableJoint`. This did not produce a good result. The `XRGrabInteractable` component is taking the grabbed object out of the parent game object. This is messing with the relative position and orientation. We have also tried using an external open source script, but that did not work as well. In the end, we have solved the problem by creating a charge handle animation, and playing that animation when the player interacts with the handle, as well as updating the logic for reloading if necessary.

## Damage(Zombie and player)

Damage was started off by having an interface that will take damage to a game object that has health, such as a zombie and player.

Also, the grenade was, when exploded, it damages all the players that implement damage so a player and zombies can take damage.

## Health(Zombie and player)

Health was started off by making a script that will be attached to the player, but later added scripts for a Zombie AI to have health.

initial health is 100, then decreased by the damage dealt to it; also, when a grenade explodes in proximity to a player, it will impact the health.

## HUD

The HUD is a game object that is placed slightly in front of the camera, and it follows the camera's orientation and position. Text for the ammo and health are sprites (number sprites), that get updated based on a main component of the HUD that controls the logic of the HUD.

## Zombie AI

As we thought about ways of creating some sort of objective for the game, we remembered one of the most loved and original mods that CS 1.6 had, the Zombies.
In terms of implementation, it was also a doable task in the time we had.
There are a few issues with the current Zombies, but those are only due to time constraints. Some of these issues are the lack of a more complex hitbox, and the sometimes glitchy movement, even though the latter one added some sort of surprise element.
As for where the zombies spawn, we made it so there would be a few points on the map that have a spawner, and the amount of zombies would increment every time the player killed 4 zombies. These were also used later on to spawn Magazines for the AK, as to add more objectiveness to the player.

## Sounds

In order to add ambiance to the game, the sound options were carefully chosen. In a way, we wanted to maintain the nostalgic feeling of CS, so the basic sounds were all taken from the original CS 1.6. The Zombie's sounds were taken from Half Life 2 (Reversed Sound), and the only original SFX was the Dying zombie sound, we could not find the Half Life version on the internet.

For the last touches, we added special sounds that would be played at random whenever the player got 4 kills.

And finalizing, we opted to add Doom Soundtrack, as we considered it was in the same nostalgic category as CS, as well as that it would be a perfectly fitting music for the kind of anxiety we wanted to recreate.

## Map changes

Experimented with some different placements of the magazines so the gameplay is more fun/immersive.
added the fog particle and changed the skybox to a darker one so it suits the zombie mode gameplay better.

## Conclusion

When the group started merging the code from different branches, some issues occurred due to overlapping code in certain scripts, prefabs, and mechanics. After we merged, the game was working perfectly as intended, fulfilling all of our requirements.