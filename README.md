# HIV Stories

**AIDS, Poverty & Faith in Mamelodi Township, South Africa**

A master's thesis project by Nathan Clendenin, UNC Chapel Hill School of Journalism and Mass Communication.

Five audio-photo documentary stories, originally built in Adobe Flash (2006). Rebuilt in modern HTML/CSS/JavaScript.

## Site Structure

```
/
├── index.html          ← Story selection page
├── story.html          ← Audio-synced photo player
├── stories.js          ← All story data (converted from stories.xml)
└── _headers            ← Cloudflare Pages cache/security headers
```

Media (images and audio) is served from Cloudflare R2 at `https://media.hivstories.org`:

```
https://media.hivstories.org/images/gravedigger/
https://media.hivstories.org/images/margaret/
https://media.hivstories.org/images/granny/
https://media.hivstories.org/images/selina/
https://media.hivstories.org/images/facing/
https://media.hivstories.org/audio/gravedigger.mp3
https://media.hivstories.org/audio/margaret.mp3
https://media.hivstories.org/audio/granny.mp3
https://media.hivstories.org/audio/selina.mp3
https://media.hivstories.org/audio/facing.mp3
```

## Stories

1. **Handling Death** — William Motsoko, Gravedigger (2:44)
2. **Dying with Dignity** — Margaret Hodany, Hospice Nurse (1:43)
3. **Pulling with One Gear** — Mabel Malobola, Grandmother (2:00)
4. **Living Positively** — Selina and Vuci, Living with HIV (2:59)
5. **Facing the Future** — Faces of Orphans (1:36)

## Player Features

- Audio plays automatically, advancing slides on cue from `stories.js` timestamps
- Pause/play stops and resumes audio + slideshow together
- Manual prev/next arrows seek audio to that slide's start time
- Keyboard: `←` `→` to navigate, `Space` to pause
- Touch: swipe left/right on mobile
- Progress bar is clickable/seekable
- Story navigation dots (right side, desktop)
- Crossfade transitions between slides

## Deployment

Hosted on Cloudflare Pages at [hivstories.org](https://hivstories.org).
Connected to GitHub repo `strydrvn/hivstories` for automatic deployment on push to `main`.
