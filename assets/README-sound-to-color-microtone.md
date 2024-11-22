# Microtonal 12x12 Frequency Grid

This project is an interactive, web-based grid that allows users to explore microtonal frequencies through sound and color. Each cell in the 12x12 grid represents a unique frequency, visualized with a color corresponding to its frequency range. Users can click on cells to hear the tones, making it an educational and experimental tool for understanding the relationship between color, frequency, and sound.

## Features

- **12x12 Grid of Tones**: Each cell represents a unique frequency, spaced evenly between a minimum (100 Hz) and maximum (5000 Hz) range.
- **Color Mapping**: Each frequency is assigned a color on a rainbow gradient, allowing for visual distinction between frequencies.
- **Playable Tones**: Clicking on a cell triggers an oscillator to play a tone at the cell's frequency, providing an interactive sound experience.
- **Responsive Hover Effect**: Cells highlight upon hover to enhance the interactive experience.
- **Frequency Labeling**: Each cell displays its frequency in Hz, providing a clear reference for users interested in specific tonal values.

## Installation and Usage

### Requirements

- **Web Browser**: Works best on modern web browsers that support the Web Audio API (tested on Chrome, Firefox, Safari).
- **Internet Connection**: No external dependencies are required after the initial load of D3.js from the CDN.

### Setup and Running Locally

1. **Clone the Repository**:
```bash
git clone https://github.com/yourusername/microtonal-frequency-grid.git
cd microtonal-frequency-grid
```
2. Open the HTML File:

- Simply open the index.html file in your preferred web browser.
3. Explore the Grid:

- Click on each cell to hear the tone at that frequency.
- Observe the color change and frequency displayed within each cell.



### Usage Instructions

1. **Click on a Cell**:
   - Each cell plays a unique frequency in the range of 100 Hz to 5000 Hz.
   
2. **Hover Effects**:
   - Cells brighten slightly on hover for a visual indication.

3. **Frequency Labels**:
   - Each cell has a label displaying the frequency in Hz, rounded for readability.


## Code Structure

- **HTML**: The `index.html` file contains the main structure and includes the D3.js library for SVG manipulation.
- **JavaScript**: The `<script>` section within the HTML defines the logic for generating frequencies, color mapping, and sound playback.
  - **Constants**:
    - `minFreq` and `maxFreq` set the frequency range.
    - `numRows` and `numCols` define the grid dimensions.
  - **Functions**:
    - `getColor(freq, minFreq, maxFreq)`: Maps each frequency to an HSL color for visual display.
    - `playTone(frequency)`: Creates an oscillator to play the sound at the specified frequency.
- **CSS**: Basic inline CSS styles are used to define the layout and hover effects for each cell.


## Future Enhancements

Here are some potential features to expand the functionality and usability of the Microtonal Frequency Grid:

1. **Polyphonic Sound**: Allow multiple frequencies to play simultaneously to create chords and harmonic structures.
2. **Oscillator Variations**: Enable users to select different oscillator types (e.g., sine, square, sawtooth) for varied tonal textures.
3. **Advanced Visualization Options**: Introduce waveform animations or oscillation visualizations within each cell to better represent the sound characteristics.
4. **Frequency Sequencer**: Add a mode to sequence cell clicks for rhythm and melody creation.
5. **Save & Share**: Provide a way for users to save frequency patterns or sequences and share them with others.
6. **Expanded Frequency Range and Tuning Systems**: Allow users to explore other tuning systems (e.g., Just Intonation, Pythagorean) and expand the grid to cover more frequencies.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [D3.js](https://d3js.org/) for visual manipulation.
- Uses the Web Audio API for sound playback.
- Inspired by studies on the relationship between color, frequency, and sound perception.
