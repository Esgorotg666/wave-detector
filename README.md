# Wave Detector

A simple Progressive Web App (PWA) that monitors your phone's sensors for unusual activity while the app is open.

## What it monitors (foreground only)

- **Motion / vibration**: Uses DeviceMotion to detect acceleration deviations from gravity.
- **Magnetic / heading shifts**: Uses DeviceOrientation (including `webkitCompassHeading` on iOS) to watch for sudden compass changes.
- **Audio spectrum**: Uses the microphone + Web Audio API to watch low-frequency and high-frequency energy (possible ultrasonic or pulsing sound).

## Limitations (important)

- **No true background monitoring** on iOS. Apple does not allow web apps to continuously access sensors when the screen is off or the app is backgrounded.
- The web DeviceOrientation API does **not** give raw magnetometer values in µT the way native apps do. It is mainly heading data.
- It cannot detect electric fields, radio-frequency energy, or sophisticated directed-energy devices.
- Best used as a quick local check for vibration or strong nearby magnetic/audio sources.

## How to use

1. Open the site on your iPhone in Safari.
2. Tap Share → Add to Home Screen to install as a PWA.
3. Open the installed app and tap **Start Monitoring**.
4. Grant motion and microphone permissions when asked.
5. Keep the app open and the screen on. Alerts appear on-screen and as notifications if permission is granted.

## Deploy

This is a static site. You can host it on GitHub Pages, Vercel, or any static host.

**Disclaimer**: This tool is for personal experimentation only. Persistent unexplained physical sensations should be discussed with a doctor.
