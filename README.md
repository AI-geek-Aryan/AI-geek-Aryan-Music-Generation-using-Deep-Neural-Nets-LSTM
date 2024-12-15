# AI-geek-Aryan-Music-Generation-using-Deep-Neural-Nets-LSTM

# Music Generation using Deep Neural Nets

This project demonstrates the generation of music using deep learning techniques, specifically utilizing Long Short-Term Memory (LSTM) networks. The primary focus is to train a neural network on MIDI files and generate new compositions based on the learned patterns.

## Table of Contents

- [Project Description](#project-description)
- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Model Details](#model-details)
- [Dataset](#dataset)
- [Results](#results)
- [Future Improvements](#future-improvements)

---

## Project Description

This project uses MIDI files as input to train a deep neural network. The network learns the patterns and structures of the musical compositions, enabling it to generate original music sequences. The generated music is saved as a MIDI file and can be played back using any MIDI player.

## Features

- Parses and preprocesses MIDI files to extract notes and chords.
- Converts musical notes into a format suitable for training a neural network.
- Generates music sequences using an LSTM-based architecture.
- Outputs the generated music as a MIDI file.

## Requirements

To run the project, install the following Python libraries:

```bash
pip install music21 tensorflow numpy pickle
```

## Usage

1. Clone the repository:

```bash
git clone <repository_url>
cd Music-Generation-using-Deep-Neural-Nets
```

2. Place your MIDI files in the `midi_songs/` directory.

3. Run the script to preprocess the MIDI files, train the model, and generate new music:

```bash
python music_generation.py
```

4. The generated music will be saved as `test_output.mid`.

## File Structure

```
Music-Generation-using-Deep-Neural-Nets/
├── midi_songs/          # Directory containing input MIDI files
├── notes                # Pickle file storing preprocessed notes
├── model.keras          # Trained model weights
├── test_output.mid      # Generated MIDI file
├── music_generation.py  # Main script
├── README.md            # Project documentation
```

## Model Details

The model is built using Keras and consists of the following layers:

- Three LSTM layers, each with 512 units, for sequence processing.
- Dropout layers to prevent overfitting.
- Dense layers to map LSTM outputs to note probabilities.
- Output layer with a softmax activation for note prediction.

### Training Parameters

- Sequence Length: 100
- Batch Size: 64
- Epochs: 10
- Loss Function: Categorical Crossentropy
- Optimizer: Adam

## Dataset

The dataset comprises MIDI files placed in the `midi_songs/` directory. The notes and chords are extracted and stored in a pickle file for preprocessing.

## Results

- The model generates music sequences based on the patterns in the input dataset.
- Output is saved as a MIDI file (`test_output.mid`).
- Example snippet of generated notes:

```
['C4', 'E4', 'G4', 'D4', 'F#4', 'A4', 'E4+G4+C5']
```

## Future Improvements

- Increase the number of training epochs and add more MIDI files to improve the model's performance.
- Experiment with different neural network architectures such as GRU or Transformer models.
- Introduce additional preprocessing techniques to handle variations in MIDI files.
- Provide a web-based interface for users to upload MIDI files and download generated compositions.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

Happy music generation! 🎵

For any questions, suggestions, or issues, feel free to contact me at [aryan070sharma@gmail.com]

