# Room Sandbox

Drop 3D objects into your room at true size using your phone camera.

**Live:** https://jdaza13.github.io/ar-viewer/

| Object | Real-world size | Animations |
|---|---|---|
| Cat | 48 cm tall (tail up), 61 cm long | Idle, walk |
| Kitten | 24 cm tall, 31 cm long | Idle, walk |
| Big dog (husky) | 85 cm tall, 1.04 m long | Idle, walk, run, jump, eat, bark… |
| Sport bike | 2.05 m long, 1.19 m tall | — |
| Cube | 10 × 10 × 10 cm | — |

You can also load your own `.glb` from the phone (it never leaves the device).

## How AR works here
- **Android (Chrome):** WebXR, falls back to Google Scene Viewer (ARCore).
- **iPhone/iPad (Safari):** AR Quick Look; the USDZ is generated on the fly.
- **True size** on = locked real-world scale; off = pinch to resize in AR.
- Deep link to an object: `#cat`, `#kitten`, `#big-dog`, `#sport-bike`, `#cube-10cm`.

## Add an object
1. Put a `.glb` in `models/` at real scale (meters), resting on y = 0.
2. Add a thumbnail PNG to `thumbs/`.
3. Add an entry to `OBJECTS` in `index.html`.

## Credits
- Cat & kitten: Quaternius, *Animal Pack Vol.2* — CC0 (kitten recolored and scaled).
- Big dog: Quaternius, *Ultimate Animated Animal Pack* (Husky) — CC0.
- Sport bike: generated with MediaGeni's [Low Poly Motorcycle Generator](https://github.com/mediageni/LowPolyMotorcycleGenerator) — MIT.
- 10 cm cube: made for this project.
- Viewer: [model-viewer](https://modelviewer.dev) (Apache-2.0), vendored in `vendor/`.

All models were decompressed and rescaled to real-world size for AR compatibility.
