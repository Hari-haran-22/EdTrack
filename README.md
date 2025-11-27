# EduTrack

An interactive student dashboard prototype focused on attendance marking, study task tracking, and schedule visualization. It demonstrates a polished front‑end UI with multiple simulated attendance methods (QR, Bluetooth proximity, Face ID), dark/light theme persistence, and a responsive layout optimized for both mobile and desktop.

## Features
- **Login Simulation**: Demo login flow (pre‑filled credentials) with transition into the app view.
- **Responsive Sidebar Navigation**: Mobile slide‑in menu + desktop sidebar with active state styling.
- **Dark Mode Persistence**: Remembers user preference via `localStorage` and respects system preference fallback.
- **Attendance Module**:
  - QR code display + (simulated) scanning using `html5-qrcode` (requires serving over HTTP/HTTPS – browsers block camera on local `file://`).
  - Bluetooth proximity & Face ID panels (simulated interactions with animated states).
  - Smart overlay indicating active/free class periods.
- **Task Suggestions Panel**: Animated progress bars and toast notifications on completion.
- **Timetable View**: Clean weekly grid with time slots and subject color coding.
- **Curriculum Progress**: Major/Minor cards with completion percentages and status badges.
- **Achievements & History**: Recent badges and attendance record table styling.
- **Toast Notifications**: Reusable success feedback component.

## Tech Stack
- **HTML + Tailwind Utility Classes** (pre‑built classes assumed via CDN or build – ensure you include Tailwind if not already)
- **jQuery** for concise DOM manipulation and event handling.
- **Font Awesome** for iconography.
- **html5-qrcode** (optional) for QR scanning (add the script if enabling live scan).

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/Visvatharsan/EduTrack.git
   cd EduTrack
   ```
2. Open `index.html` with a local HTTP server (needed for camera access):
   - VS Code: Use the Live Server extension.
   - Python quick serve:
     ```bash
     python -m http.server 5500
     ```
     Then visit: `http://localhost:5500/index.html`
3. Ensure required external CDNs (Tailwind, jQuery, Font Awesome, html5-qrcode) are referenced. If missing, add their `<script>` / `<link>` tags.

## QR Scanning Note
Camera usage will fail under `file://` protocol. Always run via a local server or deploy under HTTPS. The UI gracefully shows a warning if accessed locally without proper protocol.

## Project Structure
```
index.html   # Main interactive dashboard UI
README.md    # Project documentation
```

## Customization Ideas
- Replace mock student data and avatars with dynamic values.
- Integrate real authentication & attendance backend.
- Persist task progress in localStorage or a database.
- Add accessibility improvements (ARIA roles, focus management).

## Troubleshooting
- **QR camera blocked**: Serve over HTTP/HTTPS.
- **Icons not appearing**: Verify Font Awesome CDN link.
- **Tailwind classes ineffective**: Include Tailwind build or CDN.
- **Push rejected**: If remote already has commits, pull/rebase or force push if appropriate.

## License
Currently unspecified. Add a license (e.g., MIT) if you intend open-source distribution.

## Contributing
Open to suggestions—feel free to fork and propose UI/UX enhancements.

---
Built as a front‑end showcase for an education dashboard experience.
