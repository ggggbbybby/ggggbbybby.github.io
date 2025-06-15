---
layout: post
title:  "Twill Labyrinths"
excerpt: "these twills are a-maze-ing"
date:   2025-06-14
project: true
preview: maze.jpg
tag:
- weaving 
comments: false
---

![a maze-like twill](/assets/img/maze-hero.jpg)

I love the names that we have for various types of weaving. Lately I've been working on a warp that uses a "Double Two-Tie" threading - it uses 2 shafts for "ties", and the rest are used for pattern blocks, two per block. (A more common tied threading is Summer & Winter, which uses a single pattern shaft for each block. You could call it "Single Two-Tie" but nobody does that.) The tie-down shafts move in a regular pattern, like a steady drumbeat keeping the rest of the band focused and in-sync.

On my 8 shaft loom, I have 6 pattern shafts available, or 3 blocks. Each block is weaving a standard 2/2 twill, and the blocks can be controlled independently. (The blocks can weave other structures, plainweave or basketweave or double-faced cloth or huck texture or ...) This isn't very exciting information without a picture.

![twill blocks changing directions independently](/assets/img/maze-blocks2.jpg)

This warp has both wide and narrow blocks in the threading, they are smallest at the center and the very edges of the cloth. (That's another nice thing about double two-tie: it's a unit weave! no worries about block length or floats!) In the lower half of the image, they are weaving a big extended point twill, and all of the blocks in the center are going in the same direction. Halfway up, some of the inner blocks start wiggling back and forth, and that's what creates the heart in the center. When a block changes direction, the last pick of the old block and the first pick of the new block are the same, creating a double-thick pick. The rest of the blocks continue in the same pattern and they do not have a doubled pick. (where does it go? good question.) This kind of thing is fascinating to me! 

I really like the way that the twill lines zig and zag into little mazes. In addition to complex labyrinth patterns, you can create a surprising number of motifs and hearts and little owls with this technique. (I have always thought that the Ms & Ws point twill shapes look like owls.) The blocks can be as large as I need them to be, or as small as single 4-pick repeat. This is both exciting and overwhelming for me. The treadling for these patterns looks extremely complicated and it was hard for me to remember my sequence at first, so I had to write it down and tape it to my loom. As I wove it over and over again, I observed some interesting patterns.

1. The tie-down shafts do not alternate on every pick. They have a "base" pattern that always goes 1-2-2-1.
2. I never change the tie-downs and the pattern shafts at the same time. If the tie-downs switch, I can leave the pattern shafts where they are (and vice versa).
3. For each pair of shafts, only one is "on" at any given time. The pattern shafts act as opposites and they _all_ flip on the 3rd pick of the sequence.

With that, we can simplify my treadling instructions a little. I only have to remember the first pick of each sequence, but that's still 12 numbers in an arbitrary order and too much to keep in my head. 

There are only a few "valid" pattern shaft combinations if we follow the 3 rules above. Each pair of shafts has 2 options, which create either left- or right-leaning twill, giving us 2^3 possible options _and_ (conveniently) we can represent them with the numbers 0-7 in binary. 

![levers 1, 3, 5, 7 are down](/assets/img/maze-0.jpg)

What does "000" look like? It looks like every block starts with the odd shaft lifted. (On my loom, if a lever is in the down position, it pulls the corresponding shaft up.) All of the blocks will be weaving together in the same direction.

![levers 1, 4, 6, 8 are down](/assets/img/maze-7.jpg)
"111" looks similar, but they're all going in the other direction now. The pattern shafts lifted are exactly the opposite of the shafts lifted for 000 (but the tie-down on shaft 1 is the same).

![levers 1, 3, 6, 8 are down](/assets/img/maze-5.jpg)
"011" means that the first block is moving in one direction, while the second and third blocks are moving together in the opposite direction. It can be tricky to "see" the numbers at first. The trick is to see each pair of shaft levers as a digit - if the left/odd lever is down and the right/even lever is up, that's a "0". If the left lever is up, and the right is down, that's a "1". It gets easier with practice. 

![weaving the blocks in order](/assets/img/maze-counting.jpg)

This was a fun surprise for me: weaving the blocks "in order" from 000 to 111 creates a very pleasing symmetric motif. The sequence for weaving 0-3 is an exact mirror of the sequence from 4-7, and you can see the reflection point where _all_ of the blocks change direction. (hint: it's the thick horizontal line in the middle)


![weird wiggly diamond twill](/assets/img/maze-watermotif.jpg)
I went back to the design I wove for the beginning of the warp, it was kind of a flowy diamond shape, and analyzed the pattern using this helpful new abstraction. The first half goes 4, 2, 1, and the second half goes 7, 5, 6. I _can_ remember 6 numbers so we're in business!


![shafts labeled](/assets/img/maze-et.jpg)
I still have some warp left, so I'm trying as many number sequences as I can think of - any multi-digit number that doesn't have an 8 or a 9 in it is fair game. (8s and 9s are fine, they just get converted to 0s and 1s via modulo math.) I used a random number generator to come up with a sequence, and was overjoyed to find this weird little face looking back up at me. Someone on mastodon said it looks like ET, and I think they're right. 