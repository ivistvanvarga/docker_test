# docker_test

yum install -y epel-release.noarch &&yum  install -y docker.x86_64 docker-compose.noarch git

docker file:
 docker build -t dockertest:1 docker_files/build_test
 docker run -td --name dockertest --entrypoint /bin/bash  dockertest:1 
 docker exec -it  dockertest /bin/bash
 docker stop -it  dockertest /bin/bash
 docker tag dockertest:1 ivistvanvarga/dockertest:1
 docker push ivistvanvarga/dockertest:1

create:
docker-compose -f "docker-compose.yml" up -d --build


http://localhost/jettyapp2
http://localhost/jettyapp1

http://54.89.211.197/

destory:
docker-compose -f "docker-compose.yml" down --remove-orphans 