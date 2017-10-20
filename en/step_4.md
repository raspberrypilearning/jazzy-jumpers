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
Absolutely nothing! This is because you haven't told the parts of the jumper what to do when they hear this broadcast, so they won't do anything yet. Let's tell them what to do.
--- /collapse ---

+ Click on the **jumper** sprite

+ Add this block to the scripts.

```blocks
when I receive [new jumper v]
```

You can tell the jumper exactly what to do when it hears the broadcast by attaching the blocks you want to happen underneath this block.
