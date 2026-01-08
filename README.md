# Prerequists
## Virtual Machine
We need a Virtual Machine with a Linux environment : Ubuntu, Debian, CentOS
💡I'll continue here with an <bold>Ubuntu</bold> machine
Most important thing is that your VM must be externaly accessible (Public IP required)
We will need it for next steps

## Docker & Docker Compose
🔗https://get.docker.com/
🔗https://docs.docker.com/compose/install/standalone/#on-linux

### 🐬Docker install
First use this script
```bash
curl -fsSL https://get.docker.com -o install-docker.sh
sh install-docker.sh --dry-run
sudo sh install-docker.sh
```
Then add your current user to docker's group
On an Ubuntu Linux VM with a user called ubuntu use this command after installation 👇🏽 
`sudo usermod -aG ubuntu docker`
#Install & configure Jenkins with docker-compose
To start use those commands in a VM with docker & docker-compose isntalled 👇🏽
```bash
git clone https://github.com/Newfile01/jenkins-training.git
cd jenkins-training/
docker compose up -d
```
