# ExplorViz Docker Configurations
### Description
This repository contains docker-compose files for different configurations of ExplorViz:

- `docker-compose-X.yml`: the release version `X` of ExplorViz. 
- `docker-compose-demo-1.3.0.yml`: a [working demo of ExplorViz](http://samoa.se.informatik.uni-kiel.de:8090/) based on the latest release version.
- `docker-compose-dev.yml`: the latest development snapshot of ExplorViz.

Hint: You can change the default frontend port (8090) in the respective docker-compose file.

### Usage
1. Get the latest versions of [Docker and Docker Compose](https://www.docker.com/get-started).
2. Download one of the presented docker-compose configuration files.
3. (Prior to version 1.5.0): Adjust the `API_ROOT` variable to point to the domain or IP you will be accessing ExplorViz with. Depending on which machine you apply docker-compose, either use the machine's IP/hostname or localhost.
4. Starting ExplorViz: `docker-compose -f docker-compose-X.yml up -d`.
5. Open the frontend in your browser by accessing [http://YOUR-IP:8090](http://YOUR-IP:8090).
6. Stopping ExplorViz: `docker-compose -f docker-compose-X.yml down`. 

### Updating
1. Stop and remove all ExplorViz Docker containers: `docker-compose -f docker-compose-X.yml down`.
2. Remove all related ExplorViz Docker images: `docker rmi $(docker images "explorviz/*" -q)`.
3. Follow the [Usage](#usage) section above.
