# ExplorViz Docker Configuration Version 1.4.0

### Usage
1. Get the latest versions of [Docker and Docker Compose](https://www.docker.com/get-started).
2. Download the docker-compose configuration file.
3. Adjust the `API_ROOT` variable to point to the domain or IP you will be accessing ExplorViz with. Depending on which machine you apply docker-compose, either use the machine's IP/hostname or localhost.
4. Starting ExplorViz: `docker-compose up -d`.
5. Open the frontend in your browser by accessing [http://YOUR-IP:8090](http://YOUR-IP:8090).
6. Stopping ExplorViz: `docker-compose down`. 

### Updating
1. Stop and remove all ExplorViz Docker containers: `docker-compose down`.
2. Remove all related ExplorViz Docker images: `docker rmi $(docker images "explorviz/*" -q)`.
3. Follow the [Usage](#usage) section above.
