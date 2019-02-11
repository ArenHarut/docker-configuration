# Docker-Configuration
### Description
This repository contains docker-compose files for different configurations of ExplorViz:

- `docker-compose-latest.yml`: the latest stable version of ExplorViz. 
- `docker-compose-demo.yml`: a working demo of ExplorViz based on the latest development snapshot.
- `docker-compose-dev.yml`: the latest development snapshot of ExplorViz.

Hint: You can change the default frontend port (8090) in the respective docker-compose file.

### Usage
1. Get the latest versions of [Docker and Docker Compose](https://www.docker.com/get-started).
2. Download one of the presented docker-compose configuration files.
3. Starting ExplorViz: `docker-compose -f docker-compose-X.yml up -d`.
4. Depending on which machine you apply docker-compose, either use the machine's IP/hostname or localhost in the following.
4. Open the frontend in your browser by accessing [http://YOUR-IP:8090](http://YOUR-IP:8090).
5. Stopping ExplorViz: `docker-compose -f docker-compose-X.yml down`. 

### Updating
1. Stop and remove all ExplorViz Docker containers: `docker-compose -f docker-compose-X.yml down`.
2. Remove all related ExplorViz Docker images: `docker rmi $(docker images "explorviz/*" -q)`.
3. Follow the [Usage](#usage) section above.
