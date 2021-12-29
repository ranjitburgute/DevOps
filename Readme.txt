https://dev.to/andresfmoya/install-jenkins-using-docker-compose-4cab
https://www.youtube.com/watch?v=Z3S2gMBUkBo

docker-compose --version

mkdir ~/Jenkins

docker compose -f jenkins-docker-compose.yml up -d

docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword

Install Jenkins plugin: "GitHub Integration plugin"

ssh -R 80:localhost:8081 nokey@localhost.run

