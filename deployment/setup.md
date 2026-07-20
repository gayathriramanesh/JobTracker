# Deployment Guide

## Prerequisites

- Ubuntu 22.04 EC2
- Docker
- Docker Compose
- Nginx
- DuckDNS Domain

---

## Clone Repository

```bash
git clone https://github.com/gayathriramanesh/JobTracker.git

cd JobTracker
```

---

## Configure Environment

```bash
cp deployment/.env.example .env
```

Update

- PostgreSQL password
- Groq API Key
- Encryption key

---

## Start Containers

```bash
docker compose up -d
```

Verify

```bash
docker compose ps
```

---

## Install Nginx

```bash
sudo apt update

sudo apt install nginx
```

Copy

```bash
sudo cp deployment/nginx.conf /etc/nginx/sites-available/n8n
```

Enable

```bash
sudo ln -s /etc/nginx/sites-available/n8n /etc/nginx/sites-enabled/
```

Restart

```bash
sudo systemctl restart nginx
```

---

## Enable HTTPS

```bash
sudo apt install certbot python3-certbot-nginx

sudo certbot --nginx
```

Choose your DuckDNS domain.

---

## Verify

Open

```
"your url"
```

The n8n login page should appear.

---

## Check Logs

```bash
docker compose logs -f
```

or

```bash
docker compose logs -f n8n
```