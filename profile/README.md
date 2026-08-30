<p align="center">
  <img src="https://avatars.githubusercontent.com/u/269742371?v=4" alt="BandLive" width="120">
</p>

# BandLive

**Hackathon project for real-time collaborative music in the browser.**

BandLive lets a host create a session on a laptop while players join from their phones and perform together using simple instrument pads. Control signals travel over the network while the host synthesizes the shared audio locally. It is a hackathon prototype and project record, not an employer or operating company.

## Demo Walkthrough

1. Open the host dashboard and create a session.
2. Share the generated code or QR link with nearby players.
3. Join from phone browsers without installing an application.
4. Choose drums, bass, melody, or effects and tap the performance pads.
5. Let the server quantize inputs to the beat while the host mixes the audio.
6. Adjust tempo and transport controls from the host dashboard.

## Architecture

```text
Player phones
     |
     | Socket.IO control events
     v
Session server and beat clock
     |
     | quantized player inputs
     v
Host browser and Web Audio synthesizer
     |
     v
Shared speaker output
```

## Technical Approach

- React and TypeScript browser interfaces
- Express, tRPC, and Socket.IO server
- Server-authoritative session state and beat timing
- Web Audio API synthesis without streaming audio files
- Pentatonic note constraints to keep player combinations harmonious

## Public Repository

| Repository | Purpose |
| --- | --- |
| [band-app-v2](https://github.com/cornelljam/band-app-v2) | Full browser prototype, real-time event protocol, audio engine, and local setup guidance |

## Project Status

BandLive was built as a time-boxed hackathon collaboration. Network latency figures and deployment behavior depend on the environment and should be validated outside the demonstration setup.

[View the BandLive source](https://github.com/cornelljam/band-app-v2)
