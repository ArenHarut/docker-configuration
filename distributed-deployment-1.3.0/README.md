# ExplorViz Distributed Docker Setup
### Description

ExplorViz can be deployed in a distributed manner to spread load on multiple servers.

### Usage
1. Get the latest versions of [Docker and Docker Compose](https://www.docker.com/get-started).
2. Download all docker-compose files and copy them to your servers.
3. Modify all sections that start with `YOUR-` in every docker-compose file.
4. Start each docker-compose file: `docker-compose -f docker-compose-X.yml up -d`.
5. Open the frontend in your browser by accessing the filled out `http://YOUR-FRONTEND-IP-HOSTNAME:YOUR-FRONTEND-PORT`.
6. Stop each docker-compose file: `docker-compose -f docker-compose-X.yml down`.

### Visualizing Software
Follow our [Quick Start Guide for Users](https://github.com/ExplorViz/docs/wiki/Quick-Start-Guide-for-Users)

### Limitations
- **Scalability**: Not included. We are currently working on this.
- **Analysis/Landscape Distribution**: Due to some old legacy components, the analysis and landscape services cannot be separately deployed. We are currently working on this.
