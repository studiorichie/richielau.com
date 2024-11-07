---
layout: post
title: "Exploring Microtonal Soundscapes with a 12x12 Frequency Grid"
date: 2024-11-06 22:00:00 -0400
categories: music, microtonality, d3, sound-visualization, audio-exploration
---

In this post, I dive into the world of microtonality by creating a unique 12x12 frequency grid that visualizes and sonifies microtonal intervals. Microtonal music often ventures outside the familiar 12-tone equal temperament, instead embracing the infinite possibilities between these standardized pitches. This visualization explores an alternative sonic landscape by dividing the octave into 144 microtonal steps — a scale far finer than the typical semitone intervals in Western music.

About the Microtonal 12x12 Grid
Microtonal music can be both unfamiliar and captivating, offering subtle variations and tunings that our ears may not typically encounter. The grid you see below represents this exploration visually and sonically, presenting a 12x12 array of unique frequencies that increase gradually across the grid.

Each cell in the grid is a “microtone,” a pitch increment calculated as a small fraction of an octave. Starting from the base frequency of C4 (261.63 Hz), each frequency is separated by a very small interval — precisely the 144th root of 2, which is the factor required to divide an octave into 144 equal steps. This results in 144 unique pitches within a single octave.

Visual Representation
Each cell is displayed with a color intensity that corresponds to its pitch. Lower frequencies are represented by darker shades, while higher frequencies are progressively lighter, providing a clear visual representation of the pitch as you move across and down the grid. This gradient of brightness aligns with the increase in frequency, making the grid intuitive and visually engaging.

Lower-pitched cells: Darker shades
Higher-pitched cells: Lighter shades
Additionally, each cell is labeled with its exact frequency (rounded to one decimal), allowing you to observe the precise pitch differences as you explore.

Interaction and Sound
You can click on any cell to hear its unique frequency. The sound is generated using the Web Audio API, creating a simple sine wave that lasts for half a second. This allows you to experience the subtle tonal differences between each cell and explore the sound spectrum of this microtonal scale interactively.

Why Explore Microtonality?
Microtonal music is not only for avant-garde experimentation; it offers a rich, untapped sonic terrain that challenges conventional listening. By stepping beyond the familiar, you might discover new tonal colors, unexpected harmonies, and a sense of pitch fluidity that isn't found in traditional scales.
<!-- Embed the visualization via iframe -->
<div style="text-align: center;">
    <iframe src="/assets/sound-to-color-microtone" width="950" height="600" frameborder="0"></iframe>
</div>
