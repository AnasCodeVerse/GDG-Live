# GDG Live: event schedule and visitor guide

**A mobile-first web page built for visitors at DevFest Berlin 2026 to see, on their phones, what's on right now, what's next, where each room is, and to save the talks they wanted to attend.**

**Live page:** https://anascodeverse.github.io/GDG-Live/

---

## The problem

DevFest Berlin had 33 talks across six rooms, a hackathon and a lounge on three floors. A PDF schedule doesn't tell you which talk is starting *now*, and it's hard to read on a phone.

## What it does

- **Live now and up next.** The page reads the clock, highlights the sessions running right now and shows what starts next, with a countdown ("in 12 min"). It refreshes itself every 30 seconds.
- **Filter by room** to follow one track.
- **★ My sessions.** Tap the star on any talk to build a personal schedule. It's saved on the visitor's phone (localStorage), so no sign-up is needed.
- **Speakers list** and a **floor map** you can tap to zoom.
- **"Good to know"** section: where check-in, food, the hackathon and each room are.
- **Announcement banner** organisers can switch on for last-minute changes ("Lunch moved to 1:30 PM").
- **Dark mode** that follows the phone's setting.

## How it's built

- **One self-contained `index.html` file** with plain HTML, CSS and JavaScript. There's no framework, no build step and no backend, so it loads fast on weak venue Wi-Fi and can be hosted anywhere for free.
- **Organisers edit one block.** All event details (name, date, timezone, rooms, sessions, announcement) live in a clearly marked config section at the top of the script, so a non-developer can update the schedule on the day.
- **Timezone-aware.** Session times are stored in the event's timezone, so "now" is correct even if a visitor's phone is set to another timezone.
- **The floor map is embedded** in the file as an image, so the whole page works as a single file.

## Reuse it for your own event

1. Fork the repo.
2. Edit the `EDIT EVENT DETAILS HERE` block in `index.html` with your event name, date, timezone, rooms and sessions.
3. Turn on GitHub Pages (Settings → Pages → deploy from the `main` branch).

---

**Muhammad Anas** · [LinkedIn](https://linkedin.com/in/muhammad-anas-2002ma) · anasyounas2002@gmail.com
