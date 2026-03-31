# Multi-Container Application with Docker Compose on AWS EC2

Deployed a multi-container application using Docker Compose on a live AWS EC2 instance with Nginx and Apache running together.

---

## What it does

- Runs Nginx and Apache as separate containers on the same EC2 instance
- Configures custom port mapping for each service
- Containers communicate through a Docker network
- Accessible via EC2 public IP

---

## Tech Stack

- Docker
- Docker Compose
- Nginx
- Apache
- AWS EC2
- Linux (Ubuntu)

---

## Port Mapping

| Service | Port |
|---------|------|
| Nginx   | 80   |
| Apache  | 8081 |
| Apache  | 8082 |

---

## Project Structure
```
docker-compose-project/
├── docker-compose.yml    # Multi-container config
├── nginx/
│   └── default.conf      # Nginx configuration
└── apache/
    └── Dockerfile        # Apache container setup
```

---

## How it works

Docker Compose reads the `docker-compose.yml` file and spins up both Nginx and Apache containers with the correct port mapping and networking configured. Both services are accessible via the EC2 public IP on their respective ports.
