# Synthwave Skyline

> The city pulses when you play music. A real-time synthwave visualizer powered by your microphone.


## About

Synthwave Skyline is a browser-based audio visualizer that generates a procedural neon cityscape and animates it in real time using your microphone input. Each building is assigned its own frequency bin, so the city feels alive — bass moves the background towers, mids pulse through the middle layer, and highs drive the foreground spires. The ground grid flashes on bass hits.

Built with vanilla JavaScript, Web Audio API, and Canvas. No frameworks, no dependencies, no build step.

## Features

- Real-time microphone input via Web Audio API
- Three depth layers of procedurally generated buildings, each reacting to different frequency bands
- Per-building frequency assignment and independent lerp speeds for organic movement
- Neon glow effects with cyan and magenta color palette
- Perspective ground grid that pulses on bass hits
- Fullscreen canvas that adapts to any screen size

## Getting Started

No install needed. Just open the file.

```bash
git clone https://github.com/yourusername/synthwave-skyline
cd synthwave-skyline
open index.html
```

When prompted, allow microphone access. Play some music and watch the city react.

## How It Works

The Web Audio API feeds microphone input into an `AnalyserNode` with an FFT size of 2048, producing a frequency data array each frame. Buildings are generated on load with randomized widths, heights, lerp speeds, and frequency bin assignments. Each frame, building heights lerp toward their target frequency value, creating smooth independent movement across the skyline.

**Frequency mapping:**
- Background layer — sub-bass (bins 2–10), slow and wide
- Mid layer — bass and low-mids (bins 10–40), medium reactivity  
- Foreground layer — mids and highs (bins 40–100), fast and snappy

## Built With

- Web Audio API
- HTML Canvas
- Vanilla JavaScript

## License

MIT
