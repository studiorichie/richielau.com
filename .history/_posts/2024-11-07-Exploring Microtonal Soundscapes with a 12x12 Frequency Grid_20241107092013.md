---
layout: post
title: "Exploring Microtonal Soundscapes with a 12x12 Frequency Grid"
date: 2024-11-07 9:00:00 -0400
categories: music, microtonality, d3, sound-visualization, audio-exploration
---

In this post, I dive into the world of microtonality by creating a unique 12x12 frequency grid that visualizes and sonifies microtonal intervals. Microtonal music often ventures outside the familiar 12-tone equal temperament, instead embracing the infinite possibilities between these standardized pitches. This visualization explores an alternative sonic landscape by dividing the octave into 144 microtonal steps — a scale far finer than the typical semitone intervals in Western music.

**About the Microtonal 12x12 Grid**
Microtonal music can be both unfamiliar and captivating, offering subtle variations and tunings that our ears may not typically encounter. The grid you see below represents this exploration visually and sonically, presenting a 12x12 array of unique frequencies that increase gradually across the grid.

Each cell in the grid is a “microtone,” a pitch increment calculated as a small fraction of an octave. Starting from the base frequency of C4 (261.63 Hz), each frequency is separated by a very small interval — precisely the 144th root of 2, which is the factor required to divide an octave into 144 equal steps. This results in 144 unique pitches within a single octave.

**Visual Representation**
Each cell is displayed with a color intensity that corresponds to its pitch. Lower frequencies are represented by darker shades, while higher frequencies are progressively lighter, providing a clear visual representation of the pitch as you move across and down the grid. This gradient of brightness aligns with the increase in frequency, making the grid intuitive and visually engaging.

Lower-pitched cells: Darker shades
Higher-pitched cells: Lighter shades
Additionally, each cell is labeled with its exact frequency (rounded to one decimal), allowing you to observe the precise pitch differences as you explore.

**Interaction and Sound**
You can click on any cell to hear its unique frequency. The sound is generated using the Web Audio API, creating a simple sine wave that lasts for half a second. This allows you to experience the subtle tonal differences between each cell and explore the sound spectrum of this microtonal scale interactively.

**Why Explore Microtonality?**
Microtonal music is not only for avant-garde experimentation; it offers a rich, untapped sonic terrain that challenges conventional listening. By stepping beyond the familiar, you might discover new tonal colors, unexpected harmonies, and a sense of pitch fluidity that isn't found in traditional scales.
<!-- Embed the visualization via iframe -->
<div style="text-align: center;">
    <iframe src="/assets/sound-to-color-microtone" width="800" height="800" frameborder="0"></iframe>
</div>

1. **"How to Disappear Completely" – Radiohead**

Not strictly microtonal, but Radiohead’s atmospheric textures and unconventional song structures make it feel exploratory. Check out Kid A and Amnesiac albums for some microtonal-adjacent vibes.

2. **Wendy Carlos**
An early pioneer in electronic music and microtonality, Wendy Carlos’s Beauty in the Beast dives deep into alternate tunings with synthesized textures. It's one of the most iconic microtonal records.

3. **Aphex Twin**
Known for his experimental approach, especially in albums like Drukqs and Selected Ambient Works. "Avril 14th" and "Acrid Avid Jam Shred" hint at dissonant, tonal experiments, though not explicitly microtonal, they push the boundaries.

4. **King Gizzard & The Lizard Wizard**
Specifically, their album Flying Microtonal Banana uses microtonal tunings throughout. Tracks like “Rattlesnake” and “Billabong Valley” show how microtonal rock can be punchy and psychedelic.

5. **Young Thug**
In hip-hop, Young Thug’s vocal delivery often feels microtonal in approach, stretching into unusual tonal territory. Beautiful Thugger Girls has tracks that feel exploratory in this sense.

6. **Holly Herndon**
An avant-garde electronic artist who creates rich, layered soundscapes, often with non-standard tuning. PROTO is a good example of her unconventional electronic work.

7. **Squarepusher**
Ufabulum and other albums are electronic but feel quite experimental, with some tonal effects that flirt with microtonality. “4001” is a standout for its complex structures.

8. **The Haxan Cloak**
Dark, textural, and ambient music that brings an unsettling, droning quality to microtonal experimentation. The Excavation album has a great atmospheric depth.

9. **La Monte Young**
A minimalist pioneer in microtonality. Tracks like The Well-Tuned Piano offer pure microtonal compositions if you're looking for something meditative.

10. **James Blake**
Known for deep bass and glitchy production, songs like “Retrograde” explore harmonics in unique ways, with a sense of tonal experimentation.
This list brings you a taste of how microtonality can flow across genres, from subtle experimental tones in mainstream rock to fully microtonal compositions in electronic and avant-garde music. For more on the hip-hop front, tuning experimentation is relatively less common but can be found in artists pushing vocal and rhythmic boundaries.