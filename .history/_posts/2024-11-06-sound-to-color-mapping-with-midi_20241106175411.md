---
layout: post
title: "Sound-to-Color Mapping with MIDI"
date: 2024-11-06 17:00:00 -0400
categories: music visualization d3 midi
---

In this post, I explore how to map sound frequencies to color using MIDI data and D3.js. This interactive visualization represents musical notes as colored circles, which you can click to hear corresponding tones. The hue of each circle is based on the frequency of the note, creating a visual representation of sound.

### Visualization Setup

The visualization uses D3.js to create an SVG canvas, where each note is represented by a circle. Here's the setup code:

```html

<svg width="800" height="600" id="chart"></svg>
const keys = [
    { note: "C", freq: 261.63, midi: 60 },
    { note: "C#", freq: 277.18, midi: 61 },
    { note: "D", freq: 293.66, midi: 62 },
    { note: "D#", freq: 311.13, midi: 63 },
    { note: "E", freq: 329.63, midi: 64 },
    { note: "F", freq: 349.23, midi: 65 },
    { note: "F#", freq: 369.99, midi: 66 },
    { note: "G", freq: 392.00, midi: 67 },
    { note: "G#", freq: 415.30, midi: 68 },
    { note: "A", freq: 440.00, midi: 69 },
    { note: "A#", freq: 466.16, midi: 70 },
    { note: "B", freq: 493.88, midi: 71 }
];

function getColor(freq) {
    let hue = ((freq - 261) / (493 - 261)) * 360; 
    return `hsl(${hue}, 100%, 50%)`;
}


// Rendering Circles for Each Note

const svg = d3.select("#chart");
const width = svg.attr("width");
const height = svg.attr("height");

svg.selectAll("circle")
    .data(keys)
    .enter()
    .append("circle")
    .attr("class", "key-circle")
    .attr("cx", (d, i) => (i + 1) * (width / (keys.length + 1)))
    .attr("cy", height / 2)
    .attr("r", 30)
    .attr("fill", d => getColor(d.freq))
    .on("click", function(event, d) {
        showMidiLabel(d);
        playMidiTone(d.midi);
    });

svg.selectAll(".label")
    .data(keys)
    .enter()
    .append("text")
    .attr("class", "label")
    .attr("x", (d, i) => (i + 1) * (width / (keys.length + 1)))
    .attr("y", height / 2 + 50)
    .text(d => `${d.note} (${Math.round(d.freq)} Hz)`)
    .attr("fill", "black");

// Displaying MIDI Labels on Click

const midiLabel = svg.append("text")
    .attr("class", "midi-label")
    .attr("x", width / 2)
    .attr("y", height - 50);

function showMidiLabel(data) {
    midiLabel.text(`MIDI: ${data.midi} - ${data.note}`)
             .attr("x", (keys.indexOf(data) + 1) * (width / (keys.length + 1)))
             .attr("y", height / 2 - 50)
             .attr("visibility", "visible");

    setTimeout(() => {
        midiLabel.attr("visibility", "hidden");
    }, 2000);
}

// Playing Sound Using MIDI Notes

function playMidiTone(midi) {
    const context = new (window.AudioContext || window.webkitAudioContext)();
    const oscillator = context.createOscillator();
    const gainNode = context.createGain();
    oscillator.type = 'sine';
    oscillator.frequency.setValueAtTime(440 * Math.pow(2, (midi - 69) / 12), context.currentTime);
    gainNode.gain.setValueAtTime(0.1, context.currentTime);
    oscillator.connect(gainNode).connect(context.destination);
    oscillator.start();
    oscillator.stop(context.currentTime + 0.5);
}
