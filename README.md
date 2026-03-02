🎬 Bramflix v2.0 🚀

A professional, high-performance automated media & infrastructure stack. This project demonstrates advanced Docker Compose orchestration, GPU Passthrough for hardware transcoding, and a full GitOps workflow.

🏗️ System Architecture
The infrastructure is divided into four functional layers, all interconnected via a dedicated Docker bridge network (bramflix_net).

1. 📽️ Streaming & Request Layer
Jellyfin: The core media server, configured with NVIDIA GPU acceleration for seamless 4K transcoding.

Seerr (Jellyseerr): A sleek user interface for movie and TV show requests.

2. 🤖 Automation & Management (The "Arr" Stack)
Radarr: Fully automated movie management.

Sonarr: Fully automated TV show management.

Prowlarr: Centralized indexer management for tracking and downloads.

Bazarr: Automated subtitle management to ensure every file has the right subs.

3. 📊 Monitoring & Stats
Jellystat: Deep analytics and watch-history tracking.

PostgreSQL (15): High-availability database for statistics, featuring automated health checks.

Jellyfin-Exporter: Real-time metrics extraction for advanced monitoring.

4. 🏠 Entry Point
Homarr: A centralized dashboard serving as the gateway to all Bramflix services.

🛠️ Tech Highlights
Hardware Acceleration: Full NVIDIA Container Toolkit integration.

Storage Optimization: Centralized pooling allowing atomic moves and hardlinks.

Security & Isolation: Strict environment variable isolation and non-root execution.

Reliability: Automated health checks for database dependencies.

🚀 Deployment
Clone the repository:
git clone https://github.com/IsaacBrami/Bramflix-Infra.git
cd Bramflix-Infra

Configure Environment:
Create a .env file and define the following:

SECRET_ENCRYPTION_KEY

JELLYFIN_TOKEN

POSTGRES_PASSWORD

JWT_SECRET

Launch the Stack:
docker-compose up -d

📈 Dashboard Access
Once deployed, services are available at:

Homarr: :7575

Jellyfin: :8096

Jellyseerr: :5055

Jellystat: :3001

Radarr: :7878

Sonarr: :8989

Developed and Maintained by Isaac Brami
