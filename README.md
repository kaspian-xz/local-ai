# Docker Compose Project: Ollama, Open WebUI, n8n & PostgreSQL

This project sets up a local environment with the following services:

- **Ollama** – run and manage large language models.
- **Open WebUI** – a web interface for interacting with models.
- **n8n** – workflow automation platform.
- **PostgreSQL** – database backend for n8n.

---

## Prerequisites

- Docker & Docker Compose installed on your system.
- A `.env` file created in the root of the project.

---

## Environment Variables

Create a `.env` file with the following variables:

```env
POSTGRES_USER=
POSTGRES_PASSWORD=
POSTGRES_DB=n8n

POSTGRES_NON_ROOT_USER=
POSTGRES_NON_ROOT_PASSWORD=
```

⚠️ Replace the values with your own credentials before starting the containers.

---

## Usage

1. Clone this repository.
2. Create and fill in the `.env` file as shown above.
3. Start the stack:

   ```bash
   docker compose up -d
   ```

4. Access the services:
   - **Ollama** – `http://localhost:11434`
   - **Open WebUI** – `http://localhost:3000`
   - **n8n** – `http://localhost:5678`

---

## Stopping the Services

```bash
docker compose down
```

---

## Notes

- PostgreSQL credentials are loaded from `.env`.
- Ensure ports in `docker-compose.yaml` do not conflict with other applications.
