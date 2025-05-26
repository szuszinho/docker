# 🏠 HomeServer Docker Infrastructure

This repository contains the Docker-based infrastructure for my personal home server. It aims to run various services and applications in containers, ensuring easy deployment, updates, and maintenance.

---

## 📂 Project Structure

The project includes the following stacks:

- **`domoticz/`**: Docker configuration for the Domoticz home automation system, including Domoticz, an MQTT broker, and Zigbee2MQTT.
- **`media/`**: Media-related containers: Emby, Sonarr, Radarr, Bazarr, Jackett, and qBittorrent.
- **`traefik/`**: Reverse proxy and HTTPS certificate management using Traefik, with the following monitoring tools: Prometheus, Grafana, cAdvisor, and Node Exporter.
- **`.gitignore`**: Files ignored by Git.
- **`LICENSE`**: License information (MIT).

---

## 🚀 Installation and Usage

1. **Install Docker and Docker Compose**:

   Make sure Docker and Docker Compose are installed on your system. If not, follow the official [Docker installation guide](https://docs.docker.com/get-docker/) and [Docker Compose installation guide](https://docs.docker.com/compose/install/).

2. **Clone the repository**:
   ```bash
   git clone https://github.com/szuszinho/docker.git
   cd docker
   ```
3. **Set environment variables**:

   Configure necessary environment variables in a .env files, for example:

    ```env
    DOMOTICZ_URL=
    DOMOTICZ_DATA=
    
    EMBY_CONF=
    EMBY_TV=
    EMBY_MOVIES=
    ```
4. **Start the services**:
   
    Run the following commands to start the containers: 

    ```bash
    docker compose -f domoticz/docker-compose.yml up -d
    docker compose -f media/docker-compose.yml up -d
    docker compose -f traefik/docker-compose.yml up -d
    ```

## 🧩 Additional Information

- **License**: This project is licensed under the MIT License.

- **Contributing**: Feel free to contribute by opening pull requests or issues.

- **Contact**: For questions or suggestions, visit the GitHub Discussions page.
