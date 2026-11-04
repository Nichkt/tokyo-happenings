# Tokyo Happenings website

Public landing page for Tokyo Happenings, an Android app for the community events around Tokyo, in English. The app installs from this repository's [releases](https://github.com/Nichkt/tokyo-happenings/releases/latest).

The site is deliberately static: plain HTML, CSS, and a small amount of JavaScript, with no analytics, trackers, external fonts, or build step.

## Local preview

From this directory:

```powershell
python -m http.server 4173
```

Then open `http://127.0.0.1:4173/`.

## Events page

`events/` is the list of upcoming events, at <https://nichkt.github.io/tokyo-happenings/events/>. Don't edit it here: the app's private repository rebuilds it every day with the app's own search and replaces the whole folder, in a commit titled "Events for" and the date. The page itself lives in that repository's `web/` folder.

`events/data/translated/` holds the English copies of the wards' and cities' calendars, which are in Japanese. The same daily run puts their new listings into English with Gemini, and the app reads these copies.

## The app

Each release has `TokyoHappenings.apk`, the signed release build. The page's download button links to the latest one:

<https://github.com/Nichkt/tokyo-happenings/releases/latest/download/TokyoHappenings.apk>

## Deployment

GitHub Pages publishes the `main` branch from the repository root:

<https://nichkt.github.io/tokyo-happenings/>

The app's canonical privacy policy remains at:

<https://nichkt.github.io/seattle-happenings-privacy/tokyo/>
