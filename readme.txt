This is a tweak of JP LeBreton's "Ghosts" mod for Quake. You can get the Ghosts mod here: https://jp.itch.io/quake-ghosts

The Ghosts mod is a "tourism" mod that makes several changes to allow safely wandering through the levels of Quake. It also changes the soundtrack to use the Nine Inch Nails album "Ghosts I-IV". See the mod's webpage for more details.

This tweaked version of "Ghosts" restores the monsters into the levels, although they will not attack the player. You might like it if you feel that the presence of the Quake monsters is part of the ambience of the levels.


INSTALLATION

First download and install the Ghosts mod according to its own instructions.

Then take the progs.dat file from this package and use it to replace the progs.dat file in the "ghosts" directory of that installed mod. (If you want to save that original progs.dat file you can first move or copy it somewhere else for safekeeping.)


USE

Run the Ghosts mod according to its own instructions.

On Easy/Normal/Hard skills, monsters will now be present in the levels. (Different monsters may appear at different skill levels.) However these monsters will not notice the player and they cannot be touched or shot.

On Nightmare skill, no monsters are present. (Same as the original Ghosts mod behavior.)


ALTERNATE CONFIGURATIONS

You can modify the autoexec.cfg file in the "ghosts" directory to change the mod's behavior. You will see that normally that file sets "showturtle" to a value of 1, which will give the behavior described above. If you set showturtle to other values then you can get other behaviors:

If showturtle is 2: On Easy/Normal/Hard skills, monsters are present and do not notice the player, but they can be shot. They only have 1 health so they will die in one shot. It may be necessary to shoot some monsters to progress. On Nightmare skill, no monsters are present.

If showturtle is 3: No monsters are present regardless of skill setting. This is equivalent to picking the Nightmare skill in previous modes; also same as the original Ghosts mod behavior.


TECHNICAL NOTES

If you downloaded this in an archive that only contains this readme file and the progs.dat, note that the QuakeC source can be found here:
https://github.com/neogeographica/quakec/tree/ghosts_modified

To see the changes made compared to JP's mod, see:
https://github.com/neogeographica/quakec/compare/ghosts...ghosts_modified

There's a couple of decisions I had to make on how to handle monsters that are explicitly triggered when the player does something. Obviously they still shouldn't try to attack the player... but should they play their "wake up" announcement sound? (I chose "no".) Should they start to move around or stand still? (I chose "move around".) See the code comments in ai.qc for details.
