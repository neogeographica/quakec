This is a tweak of JP LeBreton's "Ghosts" mod for Quake: https://jp.itch.io/quake-ghosts

It uses skill selection (either in the start map or by explicitly setting the "skill" console variable) to change the mod behavior a bit.

In Easy (skill 0), no monsters are present. This is the original mod behavior.

In Normal and Hard (skill 1 and 2), monsters are present. However they do not notice the player and they cannot be touched or shot.

In Nightmare (skill 3), monsters still do not notice the player, but they can be touched and shot. They only have 1 health so they will die in one shot.

I'm supporting both Normal and Hard for the "monsters visible" mode, because they have different monster spawns.

Actually Easy can have different spawns too, so an alternate approach to this would be to have Easy/Normal/Hard all be "monster visible" modes, and perhaps put the "no monsters" mode only in Nightmare. However it seems a little odd to have the most pacifist mode be the hidden one.

There's a couple of decisions to make on how to handle monsters that are explicitly triggered when the player does something. Obviously they still shouldn't try to attack the player... but should they play their "wake up" announcement sound? (I chose "no".) Should they start to move around or stand still? (I chose "move around".) See the code comments in ai.qc for details.
