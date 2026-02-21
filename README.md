# Docker Compose Metabase

Run [Metabase](https://www.metabase.com/) with Docker Compose.

## Quick Start

```bash
docker compose up -d
```

Metabase will be available at [http://localhost:5433](http://localhost:5433).

## Configuration

| Setting | Value |
|---------|-------|
| Host port | `5433` |
| Container port | `3000` |
| Database | File-based (`/metabase-data/metabase.db`) |
| Restart policy | `unless-stopped` |

Data is persisted in a named Docker volume (`metabase_data`).

The `host.docker.internal` extra host is configured, allowing Metabase to connect to databases running on the host machine.

## Usage

```bash
# Start
docker compose up -d

# Stop
docker compose down

# View logs
docker compose logs -f metabase

# Stop and remove data
docker compose down -v
```
