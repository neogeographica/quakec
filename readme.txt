This is a tweak of JP LeBreton's "Ghosts" mod for Quake: https://jp.itch.io/quake-ghosts

It uses skill selection (either in the start map or by explicitly setting the "skill" console variable) and the values of the "showturtle" cvar to change the mod behavior.


If showturtle is 1:

On Easy/Normal/Hard skills, monsters are present. (Different monsters may appear at different skill levels.) However they do not notice the player and they cannot be touched or shot. On Nightmare skill, no monsters are present.


If showturtle is 2:

On Easy/Normal/Hard skills, monsters are present and do not notice the player, but they can be shot. They only have 1 health so they will die in one shot. On Nightmare skill, no monsters are present.


If showturtle is 3:

No monsters are present regardless of skill setting. This is equivalent to picking the Nightmare skill in previous modes; also same as the original Tourism mod behavior.


==============================================================================

There's a couple of decisions I had to make on how to handle monsters that are explicitly triggered when the player does something. Obviously they still shouldn't try to attack the player... but should they play their "wake up" announcement sound? (I chose "no".) Should they start to move around or stand still? (I chose "move around".) See the code comments in ai.qc for details.
