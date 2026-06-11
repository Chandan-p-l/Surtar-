# 🎹 SurTar - Web-Based Harmonium & Grand Piano Synthesizer

<p align="center">
  <img src="https://img.shields.io/badge/Web_Audio_API-Powered-blue?style=for-the-badge" alt="Web Audio API">
  <img src="https://img.shields.io/badge/HTML5-Canvas-orange?style=for-the-badge" alt="Canvas">
  <img src="https://img.shields.io/badge/Zero-Dependencies-green?style=for-the-badge" alt="Zero Dependencies">
  <img src="https://img.shields.io/badge/TailwindCSS-UI-38B2AC?style=for-the-badge" alt="Tailwind">
</p>

<p align="center">
  <b>Transform your laptop keyboard into a traditional Indian Harmonium and a Concert Grand Piano directly in the browser.</b>
</p>

---

# 🌐 Live Demo

### Play Online

👉 **Live Application**

https://YOUR_USERNAME.github.io/SurTar/

> Replace the URL above with your actual GitHub Pages deployment URL.

---

# 📖 About SurTar

**SurTar** combines the words:

* **Sur** (Musical Note / Melody)
* **Tar** (String / Spectrum)

SurTar is a highly responsive, browser-based digital instrument that converts a standard QWERTY keyboard into a playable musical interface.

Built entirely using:

* HTML5
* Vanilla JavaScript
* Web Audio API
* HTML5 Canvas
* Tailwind CSS

No installations, package managers, frameworks, or build tools are required.

Simply open the application and start playing.

---

# ✨ Features

## 🎼 Dual Instrument Engine

SurTar contains two completely independent synthesis engines:

### Traditional Indian Harmonium

Features:

* Multi-Reed Synthesis
* Acoustic Drawstops
* Swara Vibrato
* Bellows Air Simulation
* Manual Pumping Mode
* Auto Bellows Mode

---

### Concert Grand Piano

Features:

* Hammer Strike Simulation
* Harmonic Resonance Modeling
* Sustain Pedal
* String Damping
* Polyphonic Playback
* Adjustable Decay Time

---

# 🎹 Harmonium Synthesis Engine

The harmonium engine recreates the rich buzzing texture of traditional brass reeds.

## Additive Reed Synthesis

Each note combines:

* Sawtooth Oscillator (-4 cents)
* Triangle Oscillator (+4 cents)

This creates natural beating and warmth.

---

## Acoustic Stops

Three traditional reed banks are included.

| Stop   | Function         |
| ------ | ---------------- |
| Bass   | Sub-Octave (f/2) |
| Male   | Fundamental (f)  |
| Female | Octave (2f)      |

Stops can be enabled independently or combined.

---

## Swara Vibrato

Optional vibrato stop that mimics airflow fluctuations.

Parameters:

* Frequency: 6.2 Hz
* Depth: 3.5 cents

Generated using a Low Frequency Oscillator (LFO).

---

# 🌬️ Bellows System

## Auto Bellows

Provides continuous airflow.

Ideal for beginners and casual playing.

---

## Manual Bellows

Authentic harmonium experience.

Pump air using:

* Spacebar
* Mouse drag
* Touch gesture

---

## Physics-Based Air Pressure

Sound volume is directly tied to air pressure.

More air = louder sound.

No air = silence.

---

# 🎹 Grand Piano Engine

The piano engine simulates a resonant acoustic grand piano.

---

## Hammer Impulse

Each key generates a percussive hammer strike.

Created using:

* White Noise Burst
* Pink Noise Characteristics
* Fast Exponential Decay

Decay Time:

20 ms

---

## Harmonic Resonance

Five harmonic layers are generated.

| Harmonic    | Ratio |
| ----------- | ----- |
| Fundamental | 1.0   |
| Second      | 2.0   |
| Third       | 3.0   |
| Fourth      | 4.0   |
| Fifth       | 5.0   |

Each harmonic uses independent gain envelopes.

---

## Sustain Pedal

Spacebar acts as sustain pedal.

Features:

* Hold notes indefinitely
* Natural release behavior
* Smooth damping transitions

---

# 📊 Audio Visualization

SurTar includes a live oscilloscope.

Powered by:

* Web Audio AnalyserNode
* HTML5 Canvas

FFT Size:

256

---

## Dynamic Themes

### Harmonium

* Amber Spectrum
* Mahogany Wood Finish

### Piano

* Silver Spectrum
* Ebony Black Finish

---

# 🎵 Keyboard Layout

```text
 [ W ] [ E ]     [ T ] [ Y ] [ U ]     [ O ] [ P ]
[A ][S ][D ][F ][G ][H ][J ][K ][L ][; ][']
```

---

# 🎼 Natural Notes

| Key | Note | Sargam | Frequency |
| --- | ---- | ------ | --------- |
| A   | C4   | Sa     | 261.63 Hz |
| S   | D4   | Re     | 293.66 Hz |
| D   | E4   | Ga     | 329.63 Hz |
| F   | F4   | Ma     | 349.23 Hz |
| G   | G4   | Pa     | 392.00 Hz |
| H   | A4   | Dha    | 440.00 Hz |
| J   | B4   | Ni     | 493.88 Hz |
| K   | C5   | Sa'    | 523.25 Hz |
| L   | D5   | Re'    | 587.33 Hz |
| ;   | E5   | Ga'    | 659.25 Hz |
| '   | F5   | Ma'    | 698.46 Hz |

---

# 🎶 Sharps & Accidentals

| Key | Note | Sargam | Frequency |
| --- | ---- | ------ | --------- |
| W   | C#4  | re     | 277.18 Hz |
| E   | D#4  | ga     | 311.13 Hz |
| T   | F#4  | Ma     | 369.99 Hz |
| Y   | G#4  | dha    | 415.30 Hz |
| U   | A#4  | ni     | 466.16 Hz |
| O   | C#5  | re'    | 554.37 Hz |
| P   | D#5  | ga'    | 622.25 Hz |

---

# ⚙️ Controls

## Spacebar

### Harmonium Mode

Pump Bellows

### Piano Mode

Sustain Pedal

---

## Label Display Modes

Switch between:

* QWERTY Labels
* Sargam Labels
* Hidden Labels

---

# 🧠 Audio DSP Architecture

```text
                                +-------------------+
                                |    LFO (6.2Hz)    |
                                +---------+---------+
                                          |
                                          v
+-------------------+           +---------+---------+
| Reeds / Harmonics |---------->| Gain Envelope     |
+-------------------+           +---------+---------+
                                          |
                                          v
                                +---------+---------+
                                | Audio Analyzer    |
                                +---------+---------+
                                          |
+-------------------+                     |
| Hammer Impact Pop |---------------------+
+-------------------+                     |
                                          v
                                +---------+---------+
                                | Main Volume Node  |
                                +---------+---------+
                                          |
                                          v
                                +-------------------+
                                | Audio Destination |
                                +-------------------+
```

---

# 🔊 Audio Parameters

## Harmonium Envelope

| Parameter | Value  |
| --------- | ------ |
| Attack    | 0.08 s |
| Release   | 0.12 s |

---

## Piano Envelope

| Parameter | Value      |
| --------- | ---------- |
| Attack    | 0.004 s    |
| Decay     | Adjustable |
| Range     | 1s - 6s    |

---

# 🎛️ Polyphony Management

Active notes are stored in memory.

Benefits:

* Unlimited chord playback
* No clipping
* Smooth note release
* Natural decay

---

# 🚀 Installation

No installation required.

No dependencies required.

No build process required.

---

# Running Locally

1. Download repository
2. Open `index.html`
3. Click **Start Sound**
4. Start playing

---

# 🌍 Deploy Using GitHub Pages

## Step 1

Upload project files to GitHub.

Example:

```text
SurTar/
│
├── index.html
├── README.md
├── assets/
│   ├── images/
│   └── audio/
```

---

## Step 2

Open:

Settings → Pages

---

## Step 3

Select:

```text
Source: Deploy from a Branch
Branch: main
Folder: /(root)
```

---

## Step 4

Save changes.

GitHub automatically deploys the application.

Your site becomes available at:

```text
https://YOUR_USERNAME.github.io/REPOSITORY_NAME/
```

Example:

```text
https://johndoe.github.io/SurTar/
```

---

# 🎼 Custom Tuning

Modify note frequencies inside:

```javascript
const noteConfig = [
  {
    note: "C4",
    frequency: 261.63,
    isBlack: false,
    triggerKey: "a",
    label: "Sa"
  }
];
```

You can implement:

* Just Intonation
* Indian Classical Ratios
* Alternate Temperaments
* Custom Concert Pitch

---

# 🛠️ Technology Stack

| Layer         | Technology         |
| ------------- | ------------------ |
| Markup        | HTML5              |
| Styling       | Tailwind CSS       |
| Audio Engine  | Web Audio API      |
| Visualization | HTML5 Canvas       |
| Logic         | Vanilla JavaScript |
| Hosting       | GitHub Pages       |

---

# 🔤 Fonts

Google Fonts:

* Cinzel Decorative
* Playfair Display
* Inter

---

# 📸 Screenshots

Add screenshots here after deployment.

```md
![Harmonium Mode](assets/screenshots/harmonium.png)

![Piano Mode](assets/screenshots/piano.png)

![Spectrum Analyzer](assets/screenshots/spectrum.png)
```

---

# 🤝 Contributing

Contributions are welcome.

Ideas:

* MIDI Support
* Recording & Export
* Additional Indian Instruments
* Alternate Tuning Presets
* Mobile Enhancements
* Effects Rack

---

# 📜 License

MIT License

Feel free to use, modify, distribute, and extend SurTar for personal, educational, and commercial projects.

---

# 🎶 Final Note

SurTar bridges the worlds of Indian Classical Music and Western Piano performance through a lightweight browser experience.

No installations.

No plugins.

No external software.

Just open the browser and play.
