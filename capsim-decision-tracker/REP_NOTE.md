# Build Rep Note — CAPSIM Decision Tracker

**What I built:** A single-file CAPSIM simulation decision tracker that lets students input per-round decisions (R&D, Marketing, Production, Sales, HR, TQM, Finance) and instantly sees calculated metrics — projected revenue, operating spend, margin %, capacity utilization, and automation cost estimate. Data persists in localStorage and exports to JSON.

**What AI produced:** The complete HTML/CSS/JS artifact in one shot — semantic structure, responsive CSS with dark/light mode via CSS custom properties, localStorage persistence, metric calculations, round switching, and export. I prompted for a "Pain Detective" rep addressing the manual spreadsheet pain of tracking CAPSIM rounds.

**What I verified/fixed:** Verified the file opens directly in browser (no server needed), localStorage survives reload, all 11 input fields calculate correctly, round tabs switch state, JSON export downloads valid data. Fixed: added `step` attributes for cleaner numeric input, capped automation at 10, added toast notifications for save/export feedback.

**What I'd try next:** Add a "duplicate round" button to speed up similar rounds, import JSON to restore from backup, and a simple chart (Chart.js via CDN) showing margin trend across rounds. Could also integrate with the team's Supabase backend for multi-user sync.