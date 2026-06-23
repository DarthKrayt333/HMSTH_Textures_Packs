These textures are already ready to import with tool, and you're good to go!! :)

They already have proper position, the BOY's v3 head might be to big tough, but doesn't matter!! :)

You can make it back with c3d and then export bac kwith x3d and resize it back in _obj Folder and then c3d _obj folder!! :)

But for only Boy's head model swapping use 3d_batches_obj folder instead!! :) AND YOU'RE GOOD TO GO!!





Quick Start: Swap BOY's Head

Extract BOY archive:

xhda BOY.HDA BOY

Extract batches:

xbatches BOY\BOY_00000.RDTB BOY\BOY_00001.GDTB BOY


Open BOY_3d_batches_obj/model_02/batch_0005.obj


in Blender and replace with your custom head mesh.

Rebuild (use -all to auto-hide original hair):


cbatches BOY_3d_batches_obj BOY_NEW -all


Repack the HDA:

chda BOY_NEW BOY.HDA


Done! Your custom head is in the game.


⚠️ Important Limits — Watch Out!

When making your custom head mesh in Blender,

keep these PS2 engine limits in mind:

Keep RDTB size under ~2,100,000 bytes
(~2.1 MB) — the game has a max RDTB
memory limit hardcoded in SLUS_202.51
(the PS2 executable). We don't have the
tools yet to move this limit, so if your
modded RDTB grows too large, the game
will crash on load.
The smaller the RDTB, the better! 🎯

Keep your head model under ~5,000
triangles — the PS2 engine and VU1
microprogram have constraints on how
much geometry can be uploaded per frame.
Going over this can cause crashes,
flickering, or corrupted rendering.

In Blender, use the "Decimate" modifier
if your head mesh is too detailed —
reduce face count to stay under 5,000
triangles before exporting.

Check final RDTB size after rebuild —
if it's close to or over 2.1 MB, reduce
your model's triangle count and try again.

Stay within these limits and you're good
to go! 🚀