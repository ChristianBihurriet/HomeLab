# 🏠 Homelab DevOps - Infraestructura real con Docker y monitoring
![Docker](https://img.shields.io/badge/Docker-Used-blue)
![Monitoring](https://img.shields.io/badge/Monitoring-Prometheus%20%2B%20Grafana-green)
![VPN](https://img.shields.io/badge/VPN-Tailscale-purple)

Infraestructura de homelab diseñada para simular un entorno real de DevOps,
incluyendo despliegue de servicios, monitorización, networking y automatización.

El objetivo es aprender y aplicar prácticas reales de backend + infraestructura.
## 🏗️ Arquitectura

```text
Internet
   │
Tailscale VPN
   │
Nginx Proxy Manager
   │
Servicios Docker
 ├─ Grafana
 ├─ Prometheus
 ├─ Portainer
 ├─ Plex
 ├─ Media Stack (Radarr / Sonarr / Prowlarr / qBittorrent)
 └─ Pi-hole (DNS)
```
---
## 📁 Estructura del proyecto

```text
homelab/
 ├── plex/
 ├── media-stack/
 ├── grafana/
 ├── prometheus/
 ├── nginx/
 ├── pihole/
 ├── homeassistant/
 ├── mosquitto/
 ├── node-exporter/
 ├── portainer/
 ├── postgres/
 ├── samba/
 └── homepage/
 ```
---

## 🧱 Stack tecnológico

```md
- Docker & Docker Compose
- Nginx Proxy Manager (reverse proxy)
- Tailscale (VPN)
- Prometheus + Node Exporter (monitoring)
- Grafana (visualización)
- Pi-hole (DNS + adblock)
- Portainer (gestión de contenedores)
- Plex + ARR stack (media automation)
```
---
## ⚙️ Funcionalidades
- Despliegue de múltiples servicios en contenedores
- Monitorización completa con Prometheus y Grafana
- Acceso remoto seguro mediante Tailscale
- Reverse proxy centralizado
- Gestión visual de contenedores con Portainer
- Automatización de contenido multimedia

---
## 🧠 Decisiones técnicas

- Uso de Docker Compose para simplicidad y portabilidad
- Elección de Tailscale frente a exposición de puertos por seguridad
- Separación de servicios por responsabilidad (microservicios)
- Uso de reverse proxy para centralizar acceso
---
## 🚀 Demo

El entorno puede levantarse fácilmente con Docker Compose:

```bash
docker compose up -d
```
### Servicios disponibles:

| Servicio              | Descripción                          | Puerto |
|----------------------|--------------------------------------|--------|
| Grafana              | Dashboards de métricas               | 3000   |
| Prometheus           | Recolección de métricas              | 9090   |
| Node Exporter        | Métricas del sistema                 | 9100   |
| Portainer            | Gestión de contenedores              | 9443   |
| Plex                 | Media server                         | 32400  |
| Homepage             | Dashboard central                    | 3001   |
| Nginx Proxy Manager  | Reverse proxy                        | 80 / 81 / 443 |
| Pi-hole              | DNS + Adblock                        | 8080   |
---
## 🌐 Networking

- Uso de Docker networks para comunicación entre servicios
- Exposición de servicios mediante Nginx Proxy Manager
- Resolución interna mediante Pi-hole (DNS)
- Acceso remoto seguro a través de Tailscale (MagicDNS)
---
## 💾 Persistencia de datos

- Uso de volúmenes Docker para datos persistentes
- Separación entre configuración y datos
- Estructura de almacenamiento organizada por servicio
---
## 🧠 Aprendizajes

- Diseño de arquitectura basada en microservicios
- Gestión de redes y comunicación entre contenedores
- Monitorización de sistemas en tiempo real
- Uso de reverse proxy y DNS interno
- Automatización de flujos entre servicios
---
## 🛠️ Problemas resueltos
- Configuración de networking entre contenedores
- Persistencia de datos en servicios stateful
- Exposición segura de servicios sin abrir puertos públicos
- Integración de múltiples herramientas en un entorno coherente
---
## 📌 Estado actual

✔ Infraestructura base operativa  
✔ Monitoring completo (Prometheus + Grafana)  
✔ Reverse proxy configurado  
✔ DNS interno con Pi-hole  
🟡 Media stack en progreso  
🔜 SSO, logging centralizado y CI/CD
--
---
## 👨‍💻 Autor

**Christian Bihurriet** Desarrollador backend con interés en DevOps e infraestructura.

Este proyecto forma parte de mi proceso de aprendizaje para construir sistemas reales,
no solo aplicaciones aisladas.