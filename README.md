## 👋 Welcome to ampache 🚀

Web-based audio/video streaming application and file manager

## 📋 Description

Web-based audio/video streaming application and file manager

## 🚀 Services

- **app**: ampache/ampache:latest

## 📦 Installation

### Option 1: Quick Install
```bash
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/ampache/main/docker-compose.yaml" -o compose.yml
```

### Option 2: Git Clone
```bash
git clone "https://github.com/composemgr/ampache" ~/.local/srv/docker/ampache
cd ~/.local/srv/docker/ampache
docker compose up -d
```

### Option 3: Using composemgr
```bash
composemgr install ampache
```

## 🔧 Configuration

### Environment Variables

```shell
TZ=America/New_York
DISABLE_INOTIFYWAIT_CLEAN=0
```

See `docker-compose.yaml` for complete list of configurable options.

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59099

## 📂 Volumes

- `./rootfs/data/media/music` - Data storage
- `./rootfs/data/db/mysql/ampache` - Data storage
- `./rootfs/config/ampache` - Data storage

## 🔍 Logging

```shell
docker compose logs -f app
```

## 🛠️ Management

```bash
# Start services
docker compose up -d

# Stop services
docker compose down

# Update to latest images
docker compose pull && docker compose up -d

# View logs
docker compose logs -f

# Restart services
docker compose restart
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
