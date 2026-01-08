# Prerequists
## Virtual Machine
We need a Virtual Machine with a Linux environment : Ubuntu, Debian, CentOS
💡I'll continue here with an <bold>Ubuntu</bold> machine
Most important thing is that your VM must be externaly accessible (Public IP required)
We will need it for next steps

## Docker & Docker Compose
🔗https://get.docker.com/
🔗https://docs.docker.com/compose/install/standalone/#on-linux

### 🐳 Docker install
First use this script
```bash
curl -fsSL https://get.docker.com -o install-docker.sh
sh install-docker.sh --dry-run
sudo sh install-docker.sh
```
Then add your current user to docker's group
On an Ubuntu Linux VM with a user called ubuntu use this command after installation 👇🏽 
`sudo usermod -aG ubuntu docker`

### 🎏 Docker Compose install
Second use this script
```bash
curl -SL https://github.com/docker/compose/releases/download/v5.0.1/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
```
You can check docker-compose execution with `sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose`
You should now be ready to run Jenkins installation process

# 🕴🏽Install & configure Jenkins with docker-compose
To start use those commands in a VM with docker & docker-compose isntalled 👇🏽
```bash
git clone https://github.com/Newfile01/jenkins-training.git
cd jenkins-training/
docker compose up -d
```
