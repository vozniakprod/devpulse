# DevPulse 
> Lightweight, self-hosted VPS & Docker infrastructure health monitor with real-time streaming metrics.

## Overview
DevPulse is an open-source monitoring tool designed for developers and homelab enthusiasts who need real-time system insights without the overhead of heavy enterprise monitoring suites. It operates via a minimal Node.js daemon reading system telemetry and streaming metrics directly to a reactive web dashboard over WebSockets.

## Architecture
- **Collector Daemon:** Gathers CPU, memory, load average, disk space, and Docker engine statistics.
- **Transport Layer:** Bi-directional real-time communication via low-overhead WebSockets.
- **Frontend Dashboard:** Lightweight, dependency-free UI built with vanilla JavaScript, HTML5 Canvas for telemetry graphs, and Tailwind CSS.

## Roadmap & Planned Features
- [x] Initial project repository setup and architecture definition
- [ ] Core system metrics collection module (Linux `/proc` filesystem parser)
- [ ] Docker Engine Socket integration (`/var/run/docker.sock`) for container lifecycle tracking
- [ ] WebSocket server implementation with auto-reconnection and keep-alive handling
- [ ] Real-time canvas rendering engine (smooth 60 FPS charts without memory leaks)
- [ ] Alerting dispatcher (Telegram & Discord Webhooks for critical thresholds)
- [ ] SQLite time-series data aggregation and downsampling for historical metrics
- [ ] Authentication layer with JWT tokens for self-hosted instances

## License
MIT License. Created and maintained solely as an open-source tool.
