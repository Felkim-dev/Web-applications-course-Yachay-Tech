# Workshop 4 — ORM

> **Course:** Web Applications — YachayTech  
> **Topic:** Object-Relational Mapping (ORM)

---

## Project Structure

```
workshop-4-ORM/
├── client/                  # Frontend application
├── server/                  # Backend / REST API
├── db/
│   └── docker-compose.yaml  # MySQL database container
└── README.md
```

---

## Prerequisites

Before running this project, make sure you have the following installed:

- [Docker](https://www.docker.com/) (v20+)
- [Python](https://www.python.org/) (3.14+)

---

## Setup

### 1. Database — MySQL via Docker

The database runs as a Docker container managed by Docker Compose.

**Start the container:**

```bash
cd db
docker compose up -d
```

**Verify the container is running:**

```bash
docker compose ps
```

You should see the `mysql-ws4` container with status `running`.

**Stop the container:**

```bash
docker compose down
```

> **Note:** Data is persisted in the `mysql-ws4-data` Docker volume, so it survives container restarts.

#### Connection details

| Parameter | Value       |
|-----------|-------------|
| Host      | `localhost` |
| Port      | `3306`      |
| User      | `root`      |
| Password  | `root`      |
| Database  | `webshop`   |

#### Troubleshooting

- If the connection is refused right after starting, wait ~15 seconds for MySQL to initialize and try again.
- To inspect container logs: `docker compose logs -f`
