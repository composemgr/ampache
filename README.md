## 👋 Welcome to ampache 🚀

Ampache - Web-based audio/video streaming and file manager

## 📋 Description

Ampache is a web-based audio/video streaming application and file manager allowing you to access your music & videos from anywhere, using almost any internet-enabled device. Catalog and stream your entire media collection.

## 🚀 Services

- **app**: Ampache server (`ampache/ampache:latest`)
- **db**: MariaDB database

### Infrastructure Components

- **Database**: MariaDB for media catalog and metadata

## 📦 Installation

### Using curl
```shell
curl -q -LSsf "https://raw.githubusercontent.com/composemgr/ampache/main/docker-compose.yaml" | docker compose -f - up -d
```

### Using git
```shell
git clone "https://github.com/composemgr/ampache" ~/.local/srv/docker/ampache
cd ~/.local/srv/docker/ampache
docker compose up -d
```

### Using composemgr
```shell
composemgr install ampache
```

## 🔧 Configuration

### Environment Variables

```shell
# Core Settings
TZ=America/New_York
BASE_HOST_NAME=${HOSTNAME}

# Database Settings
DB_ADMIN_PASS=changeme_admin_password
DB_USER_NAME=ampache
DB_USER_PASS=changeme_db_password
DB_CREATE_DATABASE_NAME=ampache
```

## 🌐 Access

- **Web Interface**: http://172.17.0.1:59028
- **First-time setup**: Follow installation wizard
- Configure database connection using above credentials

## 📂 Volumes

- `./rootfs/config/ampache` - Configuration files
- `./rootfs/data/ampache` - Application data
- `./rootfs/data/media/music` - Music library
- `./rootfs/data/media/videos` - Video library
- `./rootfs/db/mariadb/ampache` - Database files

## 🔐 Security

- Complete setup wizard on first run
- Create admin account during installation
- Change default database passwords
- Configure user permissions appropriately

## 🎵 Usage

1. Complete installation wizard
2. Configure catalog paths (/media/music, /media/video)
3. Update catalog to scan media
4. Configure streaming settings
5. Create user accounts
6. Start streaming!

## 🔍 Logging

```shell
docker compose logs -f app
docker compose logs -f db
```

## 🛠️ Management

```shell
# Start
docker compose up -d

# Stop
docker compose down

# Update
docker compose pull && docker compose up -d

# Backup database
docker compose exec db mysqldump -u ampache -p ampache > backup.sql
```

## 📋 Requirements

- Docker Engine 20.10+
- Docker Compose V2+
- Media files in supported formats
- Reverse proxy recommended for external access

## 🤝 Author

🤖 casjay: [Github](https://github.com/casjay) 🤖  
🦄 composemgr: [Github](https://github.com/composemgr) 🦄
