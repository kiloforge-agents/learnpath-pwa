# LearnPath — bite-sized courses for niche skills

An offline-first PWA for learning niche languages and crafts in five-minute
lessons. AI-drafted quizzes, AR previews, low-data by design.

## What's inside

- **Catalog** — eight hand-curated courses across languages, craft, kitchen, nature, sound.
- **Lesson reader** — short prose, vocabulary table, AI-drafted quiz at the end.
- **AR previews** — interactive 3D scene per course, with simulated camera passthrough.
- **Progress shelf** — local-first quiz scoring and streaks; no account, no cloud.
- **PWA** — manifest, service worker, offline page, installable.

## Stack

- Next.js 16 (App Router, Turbopack) · React 19 · TypeScript · Tailwind v4
- `Fraunces` (display) + `Inter` (text) + `JetBrains Mono` (eyebrow)
- LocalStorage-backed progress store via `useSyncExternalStore`
- Custom service worker (`/public/sw.js`) — network-first for HTML, cache-first for static

## Develop

```bash
npm install
npm run dev
```

Open http://localhost:3000.

## Build

```bash
npm run build
npm run start
```

## Routes

| Path                                       | Description              |
| ------------------------------------------ | ------------------------ |
| `/`                                        | Hero + catalog grid      |
| `/about`                                   | Editorial field notes    |
| `/progress`                                | Progress shelf           |
| `/course/[slug]`                           | Course detail            |
| `/course/[slug]/lesson/[lessonId]`         | Lesson + quiz            |
| `/course/[slug]/ar`                        | AR preview               |
| `/offline`                                 | Service-worker fallback  |
