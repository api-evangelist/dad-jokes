# Dad Jokes (icanhazdadjoke)

APIs.json 0.19 provider profile for [icanhazdadjoke](https://icanhazdadjoke.com/) — the internet's largest selection of dad jokes, served via a free, open REST API built and maintained by Brett Langdon at C653 Labs.

## About

icanhazdadjoke offers a free, unauthenticated REST API for:

- Fetching a random dad joke
- Retrieving a specific joke by ID
- Searching jokes by keyword with pagination
- Slack slash-command (`/dadjoke`) formatted responses
- Discord bot integration
- Joke images as PNG
- GraphQL queries

No API key, account, or subscription is required. Consumers are asked to set a descriptive `User-Agent` header so the operator can identify integrations.

## API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | `/` | Random joke (JSON/text/HTML via Accept header) |
| GET | `/j/{id}` | Specific joke by ID |
| GET | `/j/{id}.png` | Specific joke as PNG image |
| GET | `/slack` | Random joke formatted for Slack |
| GET | `/search` | Search jokes (`term`, `page`, `limit` params) |
| POST | `/graphql` | GraphQL interface |

## Base URL

```
https://icanhazdadjoke.com
```

## Authentication

None required.

## Response Formats

Set the `Accept` header to control response format:

- `application/json` — JSON object
- `text/plain` — plain text
- `text/html` — HTML page (default in browser)

## Repository Contents

```
apis.yml                              # APIs.json 0.19 index
plans/dad-jokes-plans-pricing.yml     # Pricing tiers (free forever)
rate-limits/dad-jokes-rate-limits.yml # Rate limit details
finops/dad-jokes-finops.yml           # FinOps guidance for consumers
```

## Links

- Website: https://icanhazdadjoke.com/
- API Docs: https://icanhazdadjoke.com/api
- Twitter/X: https://twitter.com/icanhazdadjoke
- Creator GitHub: https://github.com/brettlangdon

## Maintainer

Kin Lane — kin@apievangelist.com
