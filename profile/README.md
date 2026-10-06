<div align="center">

# Sportykore

**Run grassroots football competitions end to end — leagues, fixtures, lineups, and live match days — from one platform.**

[Website](https://www.sportykore.com) · [Docs](https://www.sportykore.com/docs)

</div>


## What we're building

Sportykore gives organizers everything they need to run a competition — seasons, team rosters, venues,
fixtures, lineups, standings, and knockout brackets — and gives players a public home for their profile,
stats, and match history. A league created by an organizer becomes something players can discover, join,
and follow in real time, on the web or in the app.

## Repositories

| Repo | What it is | Stack |
| --- | --- | --- |
| [sportykore-app](https://github.com/SportyKore/sportykore-app) | The player & organizer mobile app — profiles, leagues, live match center | Expo / React Native, TypeScript |
| [sportykore-api](https://github.com/SportyKore/sportykore-api) | The backend powering competitions, auth, and real-time match data | AdonisJS, PostgreSQL, Redis |
| [sportykore-waitlist](https://github.com/SportyKore/sportykore-waitlist) | Marketing site, product docs, and the Kanter Ball mini-game | Astro, TypeScript |

Each repo has its own README with setup instructions. Issues and discussions live on the repo they
concern — there's no central issue tracker.

## How the pieces fit together

```
sportykore-app  ──┐
                   ├──►  sportykore-api  ──►  PostgreSQL + Redis
sportykore-waitlist┘        (AdonisJS, real-time via SSE)
```

The app and the website both talk to the same API. Competitions created by an organizer (in the app)
surface publicly on the website for discovery, and live match events stream to both over Transmit (SSE).

## Contact

Questions or partnership inquiries: **sportykore@gmail.com**
