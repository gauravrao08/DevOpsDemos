##to get the root access on jenkins inside docker container

mkdir -p /var/jenkins_home
chown -R 1000:1000 /var/jenkins_home
docker run -d -p 8080:8080 -p 50000:50000 -v /var/jenkins_home:/var/jenkins_home/ --name mycontainer jenkins/jenkins

docker exec -u 0 -it mycontainer bash
