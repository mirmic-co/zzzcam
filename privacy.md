---
title: Privacy Policy
---

# Privacy Policy

**Effective Date:** April 14, 2026
**App:** ZzzCam (package `co.mirmic.zzzcam`)

## Summary

ZzzCam is designed for privacy by default. **We do not collect, transmit, or store any of your data on servers we control.** There is no cloud account, no analytics, no advertising, and no third-party tracking.

Video and audio from the camera device stream **directly** to your paired monitor device using peer-to-peer WebRTC. Everything else (sleep events, environment readings, pairing credentials) is stored **locally on your devices only**.

## Data the App Uses

### Video and audio

- The Night Camera device captures video from its camera and audio from its microphone.
- This stream is sent **directly** to paired monitor devices over an encrypted peer-to-peer WebRTC connection.
- The stream is **not recorded, stored, or uploaded to any server** by the app.
- Connections use DTLS-SRTP encryption (WebRTC standard).

### Sleep events and environment readings

- If enabled, the app detects movement and sound events and logs them in a local database (Android Room) on the camera device.
- Ambient temperature, humidity, and battery level readings are stored locally in the same database.
- Short audio clips surrounding detected events may be cached on the camera device for playback on the monitor.
- All of this data stays on your devices. **None of it is transmitted off-device** except over your direct WebRTC connection to your paired monitor.

### Pairing credentials

- To secure the connection, the app stores a stable camera identity (UUID + friendly name), a TLS certificate and its password, and a pairing authentication token — all on your device in Android's encrypted storage.
- Credentials never leave the device they were generated on, except during the QR-code pairing flow (which transfers the token directly from camera to monitor over your local network).

### Permissions the app requests and why

| Permission | Purpose |
|---|---|
| Camera | Capture video on the night camera device |
| Microphone | Capture audio and detect sleep events |
| Foreground service | Keep the camera/monitor running while the screen is off |
| Post notifications | Show the ongoing camera/monitor status, and alert the parent to sleep events |
| Network (INTERNET, ACCESS_NETWORK_STATE) | P2P WebRTC connection over your LAN or VPN |
| Wake lock | Keep the camera device active during monitoring sessions |

## Third-Party Services

ZzzCam does not integrate with any cloud analytics, crash-reporting, or advertising services.

The app optionally works with **Tailscale**, a third-party WireGuard-based VPN service, to let the camera and monitor connect from different networks. Tailscale is an **optional** dependency that you install and manage separately on each device. ZzzCam does not send any user data to Tailscale beyond the WebRTC traffic that already flows between your paired devices; Tailscale acts purely as an encrypted network transport. Review Tailscale's privacy policy at <https://tailscale.com/privacy-policy> if you choose to use it.

## Children's Privacy

ZzzCam is a parental monitoring tool designed to be **operated by adults**. It is not directed at children under 13. We do not knowingly collect personal information from children.

Because the app does not transmit data to any server controlled by us, no data about children (or anyone else) is ever received by the app developer.

## Data Retention and Deletion

All app data is stored locally on your device. You can delete all app data at any time by:

1. Uninstalling the app, **or**
2. Going to **Settings → Apps → ZzzCam → Storage → Clear storage** on your device.

## Your Rights

Because we do not hold any personal data about you on any server, there is nothing for us to export, correct, or delete on your behalf. You have full control of your data on your own devices.

## Changes to This Policy

If this policy changes materially, we will update the effective date above and post the updated policy at this URL before the change takes effect.

## Contact

If you have questions about this policy or the app's privacy behavior, contact us at:

**[privacy@zzzcam.com](mailto:privacy@zzzcam.com)**

ZzzCam is built by [Mirmic](https://mirmic.co).
