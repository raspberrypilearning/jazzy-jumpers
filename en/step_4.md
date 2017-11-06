## New jumper

In this project there are a lot of sprites, so a good way of telling lots of sprites what to do is to send a **broadcast**.

[[[generic-scratch-broadcast-message]]]

Let's create a broadcast which tells the various sprites forming the jumper to each choose a random costume, making a new jumper.

+ Click on the **stage** and make sure you are on the scripts tab.

The stage is going to send a broadcast called "new jumper" to all of the other sprites. Think of it like a person with a megaphone giving instructions to lots of people at once.

+ Add this code to the stage. If you can't remember how to create a new broadcast message, have a look at the information above to refresh your memory.

```blocks
when flag clicked
broadcast [new jumper v]
```

+ Click the green flag. What happens? Do you see a new jumper appear?

--- collapse ---
---
title: Answer
---
Absolutely nothing happens! This is because you haven't told the parts of the jumper what to do when they hear this broadcast, so they won't do anything yet. Let's tell them what to do.
--- /collapse ---

+ Click on the **jumper** sprite in the "Sprites" panel

![Jumper](images/jumper.png)

+ Add this block to the scripts for the jumper

```blocks
when I receive [new jumper v]
```

You can tell the jumper exactly what to do when it hears the broadcast by attaching the blocks you want to happen underneath this block.

When the jumper sprite hears the broadcast, it should randomly pick one of the coloured costumes - but not the white one.

![Jumper costumes](images/jumper-costumes.png)

+ Attach some code to your `when I receive`{:class="blockcontrol"} block to tell the jumper sprite to pick a random costume out of the first three only.

```blocks
switch costume to (pick random (1) to (3))
```

+ Click the green flag. Does the jumper colour change? Click the green flag a few more times to check.

The colour might not change every single time you press the green flag, because sometimes the randomly chosen costume might be the same as the previous one.

+ Now add some code to the **stripes**, **picture** and **trim** sprites so that when they hear the broadcast "new jumper" they also choose a random costume.

--- hints ---
--- hint ---
The code you will need to use is exactly the same for all of the sprites!
--- /hint ---
--- hint ---
You can save time by duplicating the code. Drag all the code attached to the `when I receive`{:class="blockcontrol"} block on top of one of the other sprites in the "Sprites" panel and let go to drop it.

Look inside that sprite and you should see a copy of the code.
--- /hint ---
--- /hints ---
