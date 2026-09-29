# lol-discord-bot

A private Discord bot for a group of about 20 friends who play League of Legends together (KR server).

## What it does

- **Rank lookup** — each member registers their own Riot ID (`name#tag`) and the bot shows their current Solo/Flex ranked tier, LP and win rate.
- **Custom game lobby** — members join an in-house (custom) game with one button, and the bot splits the 10 players into two balanced teams.
- **In-house scoreboard** — after each custom game, the winning team is recorded and a group scoreboard is updated. This score is based only on our own recorded results, not on Riot API data.

## Riot API usage

| API | Purpose |
|---|---|
| `account-v1` (asia) | Riot ID → PUUID, once per registration |
| `league-v4` (kr) | PUUID → ranked tier, LP, wins/losses |

- Only players who register themselves are looked up.
- Results are cached and refreshed once or twice a day, so the whole group uses only a few dozen requests per day.
- The API key is kept in a server-side environment variable and never exposed to users.

## Scope

- Used only inside one private Discord server by a small group of friends.
- Not a public service. No ads, no monetization.

## Contact

GitHub: [@chahyunwoo](https://github.com/chahyunwoo)

---

lol-discord-bot isn't endorsed by Riot Games and doesn't reflect the views or opinions of Riot Games or anyone officially involved in producing or managing Riot Games properties. Riot Games, and all associated properties are trademarks or registered trademarks of Riot Games, Inc.
