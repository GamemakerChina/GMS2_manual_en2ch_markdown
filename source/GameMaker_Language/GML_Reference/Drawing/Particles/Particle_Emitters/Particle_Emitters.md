# Particle Emitters

Particle **emitters** are used by GameMaker to emit particles over an
area of the screen which can have different forms and distributions.
They can also either create a continuous stream of particles or they can
burst out a number of particles all at once, depending on the way the
functions are used. Since a particle emitter is a dynamically created
resource, you must create it and store the returned index in a variable
to reference the emitter in all further function calls, and it is very
important that you also destroy the emitter when it is no longer needed
or else you will have a memory leak that will slow down and eventually
crash your game. It is also worth noting that particle emitters will
live on forever after they are created, even if the index is no longer
stored. So even if you change room or restart the game, the systems and
the particles will remain, and be visible, in all further rooms so you
should ensure you destroy them once you no longer need them. The
following functions are available to set the emitters and to let them
create particles. Note that each of them gets the index of the [particle
system](../Particle_Systems/Particle_Systems) to which it belongs as
a first argument.

-   [part_emitter_exists](part_emitter_exists)
-   [part_emitter_create](part_emitter_create)
-   [part_emitter_clear](part_emitter_clear)
-   [part_emitter_region](part_emitter_region)
-   [part_emitter_burst](part_emitter_burst)
-   [part_emitter_stream](part_emitter_stream)
-   [part_emitter_destroy](part_emitter_destroy)
-   [part_emitter_destroy_all](part_emitter_destroy_all)
