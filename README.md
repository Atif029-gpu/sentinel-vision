# 🛡️ SentinelVision

A smart security camera that watches a room and tells you when something looks off.

It uses your webcam and a YOLO AI model, then shows everything on a live web dashboard you can open on your laptop or phone.

## What it catches

-  People walking into a restricted area you draw
- Knives (and guns, if you add a weapon model)
- Bags, laptops or phones left alone for too long
- Objects left sitting inside the restricted area

Every alert saves a snapshot photo and a line in a log file. You can also get alerts on your phone through the free ntfy app.

## The dashboard

- Live video with outlines around what the AI sees
- A status badge: OK, Warning or Alert
- An alert feed with evidence photos
- Switches to turn each feature on or off
- A tool to draw your own restricted zone right on the video

## Run it

```bash
python sentinel.py
```

Then open http://localhost:5000. On your phone, use the link printed in the terminal (same Wi-Fi).

## Quick tweaks

Everything is at the top of `sentinel.py`:

- `SOURCE`: `0` for webcam, or a phone stream link
- `UNATTENDED_SECONDS`: how long before a left-behind object triggers an alert
- `NTFY_TOPIC`: set a secret name to get phone alerts


