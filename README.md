# Sonocode

Turn a short sound clip (up to 1 minute) into an image, and play it back from the image later.

Everything runs in your browser. Nothing is uploaded anywhere.

**Live:** https://sonocode.arifdev.of.to

## How to use

1. Open the live link (or `index.html`) in a recent **Chrome or Edge** (it needs WebCodecs for Opus).
2. **Sound → Code:** upload an audio file or record with the microphone. Pick the look, maximum duration (5 s – 60 s) and quality, then press **Generate code**. Save the PNG.
3. **Code → Sound:** choose the PNG (or take a photo of a printed one). The sound is recovered and can be played or saved as WAV.

## How it works

- Audio is compressed with Opus (6 – 32 kbps).
- Reed-Solomon (255, 223) error correction is added, so small damage to the image can be repaired.
- The bytes are drawn as a grid of cells with 4 brightness levels.
- The grid is at most 300 columns wide. Longer clips make the image taller, not denser.

## Tips

- Send the image as a **file**. Chat apps shrink pictures and can damage the code, especially tall ones.
- Use a lower quality or a shorter duration for a smaller image.
- For printing, use a sharp, flat, well-lit copy.

## Limits

- Voice works best. Music at low bitrates sounds rough.
- A 60 s clip makes a very tall image (over 10,000 px at 16 kbps). Very high quality at 60 s may be refused as too large.
