# Github and Jenkins Integration'

https://dev.to/andresfmoya/install-jenkins-using-docker-compose-4cab
https://www.youtube.com/watch?v=Z3S2gMBUkBo

## GitHub VsCode:
git config --global user.name "ranjitburgute"             
git config --global user.email "burgute.ranjitkumar@gmail.com" 
git config --global --list

## Jenkins Setup using Docker:

docker-compose --version

mkdir ~/Jenkins

docker compose -f jenkins-docker-compose.yml up -d

docker exec jenkins cat /var/jenkins_home/secrets/initialAdminPassword

Install Jenkins plugin: "GitHub Integration plugin"

ssh -R 80:localhost:8081 nokey@localhost.run

## Configure Jenkins project:

GitHub Project - Project url: https://github.com/ranjitburgute/SpringConfig/
Git -> Repositories -> Repository URL: https://github.com/ranjitburgute/SpringConfig.git
Build Triggers: GitHub hook trigger for GITScm polling

## GitHub Webhooks:

Repositories -> Settings -> Webhooks
PayLoad url: https://1e071ba9b5f170.localhost.run/github-webhook/'
Just the push event
Active
