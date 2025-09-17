# HomeJellyFin

A Docker Compose setup for running Jellyfin media server.

## Quick Start

1. Clone this repository
2. Run the following command to start Jellyfin:

```bash
docker-compose up -d
```

3. Access Jellyfin at http://localhost:8096

## Directory Structure

- `data/config/` - Jellyfin configuration files
- `data/cache/` - Jellyfin cache files
- `data/media/` - Your media files (movies, TV shows, music, etc.)
- `data/transcode/` - Temporary transcoding files

## Features

- Runs on port 8096
- Auto-creates data directories if they don't exist
- Uses host networking for better performance
- Hardware acceleration support (if available)
- Proper file permissions (user 1000:1000)

## Adding Media

Place your media files in the `data/media/` directory. You can organize them as follows:

```
data/media/
├── movies/
├── tv-shows/
├── music/
└── photos/
```

## Stopping Jellyfin

```bash
docker-compose down
```

## Notes

- The data directories are automatically created when you run `docker-compose up`
- All data directories are excluded from git via `.gitignore`
- The setup uses host networking for optimal performance
