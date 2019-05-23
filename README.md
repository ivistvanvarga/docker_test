# docker_test

docker file:
 docker buid -t dockertest:1 .
 docker tag dockertest:1 ivistvanvarga/dockertest:1
 docker push ivistvanvarga/dockertest:1

create:
docker-compose -f "docker-compose.yml" up -d --build

destory:
docker-compose -f "docker-compose.yml" down --remove-orphans 