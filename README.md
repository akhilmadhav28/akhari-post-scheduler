# akhari-post-scheduler

Scheduler only: a GitHub Actions workflow that calls the Akhari social media app's
`/api/internal/run-due-posts` endpoint every 5 minutes. The app itself lives in a separate
private repository. No app code or secrets are stored here; the endpoint URL and API key are
encrypted Actions secrets.

- `run-due-posts.yml` runs every 5 minutes (and on demand from the Actions tab).
- `keepalive.yml` commits a timestamp monthly so GitHub doesn't pause the schedule.
