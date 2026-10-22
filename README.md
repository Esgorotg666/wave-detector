# Wave Detector (Improved)

PWA that monitors motion, heading shifts, and audio spectrum while open.

## New / Improved Features

- **10-second baseline calibration** — sit still and quiet, then thresholds are relative to your environment.
- **Smoothing** — exponential moving average so readings are less jumpy.
- **Adjustable thresholds** — live sliders for motion, heading, low audio, high audio.
- **Alert cooldown** — prevents notification spam (4 s minimum between alerts).
- **Color-coded values** — green → yellow → red as values approach/exceed thresholds.
- **Better spectrum drawing** — higher-DPI canvas, clearer low/mid/high coloring.
- **Exportable log** — download the event log as a text file.
- **Improved audio capture** — noise suppression and AGC disabled for rawer data.

## Limits (still true)

- Foreground only. No continuous background monitoring on iOS.
- Heading data only (not raw magnetometer µT).
- Cannot detect electric fields or RF.
- Best for spotting vibration, sudden compass jumps, or unusual audio energy nearby.

## Usage

1. Host on GitHub Pages or any static host.
2. Open in Safari → Add to Home Screen.
3. Tap **Calibrate Baseline** and stay still/quiet for 10 seconds.
4. Adjust sliders if needed, then **Start Monitoring**.
5. Keep the app open and screen on.

**Disclaimer**: Experimental tool only. Persistent unexplained sensations should be checked by a doctor.
