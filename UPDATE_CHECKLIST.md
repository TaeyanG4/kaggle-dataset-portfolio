# Portfolio Update Checklist

Use this checklist when a project changes materially. Keep this public repository free of secrets, private machine state, and personal contact information.

## Before editing

- Read `README.md` and `portfolio.json`.
- Read the affected project repository for current public facts and release invariants.
- If Kaggle state matters, refresh it from live Kaggle instead of copying an old snapshot.
- Distinguish measured/live facts from estimates or plans.

## Update the project record

Record only what is public and useful for cross-project planning:

- state: planning, pilot, building, published, maintenance, paused, or stopped
- archetype: FLAGSHIP, EVERGREEN, TREND, COMPETITION-PAINKILLER, or EXPERIMENT
- geography, modality/grain, audience, primary task
- GitHub URL and Kaggle URL when public
- public release shape, row/file/image count, and high-level size when verified
- source authority and high-level rights posture
- latest verified Kaggle status/Usability when relevant
- downloads/votes/external-adoption snapshot with an explicit `as_of` date
- important interpretation caveats
- current bottleneck and exactly one concrete next action

## Encoding integrity

- Keep repository text valid UTF-8.
- Write JSON as UTF-8 without BOM.
- Preserve Korean/non-ASCII text exactly.
- Never use lossy decode/encode settings such as silent ignore/replacement to make text pass.
- Inspect Korean/non-ASCII fields after any transcoding or generated-file rewrite.

## Never publish here

- API keys, bearer tokens, OAuth codes/access/refresh tokens
- authorization headers or cookies
- credential-bearing `.env` content
- local absolute paths or usernames embedded in paths
- machine identifiers, local process IDs, private logs/checkpoints
- private repository/account IDs
- email addresses or personal contact details
- raw personal data unless it is intentionally part of a separately reviewed public dataset release

## After editing

- Keep `README.md` and `portfolio.json` consistent.
- Validate `portfolio.json` as JSON.
- Re-open the rendered README and check links/Unicode rendering.
- Do not overwrite newer adoption metrics with an older snapshot.
- If a fact cannot be verified, mark it pending/unknown rather than guessing.
