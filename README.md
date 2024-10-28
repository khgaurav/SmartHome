# SmartHome Project
## Introduction
This project is a smart home system that contains multiple containers that are responsible for different tasks. The system is built using Docker and Docker Compose. The system is built using the following containers:
- **Home Assistant**: This container is responsible for the main logic of the system. It is responsible for controlling all the smart devices in the house which includes lights, switches, and sensors. It also provides a web interface and app to control the devices.
- **Pi-hole**: This container is responsible for blocking ads and tracking on the network. It is a DNS sinkhole that protects devices from unwanted content, without installing any client-side software.
- **Mosquitto**: This container is responsible for the MQTT broker. It is used to send messages between the different containers.
- **Tailscale**: Container is a VPN that allows the server to be accessed from anywhere.
- **Portainer**: Provides a web interface to manage the containers.
- **Frigate**: This container is responsible for interfacing with cameras around the house, record the stream and detecting objects in the camera feed and triggeing events.
- **Duplicati**: This container is responsible for backing up the data in the system.
- **Cloudflared**: Creates a cloudflare tunnel to access all the above services through my personal domain
- **Jellyfin**: This container is responsible for storing photos and media and serving them to the network
- **Bazarr**: This container is responsible for downloading subtitles for the media in Jellyfin

# Setup Instructions
## Prerequisites
- Docker
- Docker Compose
- A domain name

## Steps
1. Clone the repository
2. Replace all the placeholders in config files with your own values
3. Run the following command to start the containers
```bash
docker compose -f docker-compose.yaml -f media.yaml up -d
```
