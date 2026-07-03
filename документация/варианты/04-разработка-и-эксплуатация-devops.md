# Вариант 4: DevOps (CI/CD)

> Команды собраны из исходного материала без проверки на конкретной версии Ubuntu. Версии пакетов, ссылки и доступность Snap могут меняться.

```bash
# =====================================================
# УСТАНОВКА VS CODE
# =====================================================
sudo snap install --classic code

# =====================================================
# УСТАНОВКА DOCKER (исправлено)
# =====================================================
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker $USER
newgrp docker
docker --version

# =====================================================
# УСТАНОВКА DOCKER COMPOSE
# =====================================================
sudo apt install -y docker-compose

# =====================================================
# УСТАНОВКА JENKINS (исправлено)
# =====================================================
sudo apt install -y openjdk-17-jdk
wget -O jenkins.deb https://get.jenkins.io/debian-stable/jenkins_2.452.2_all.deb
sudo dpkg -i jenkins.deb 2>/dev/null || sudo apt --fix-broken install -y
sudo dpkg -i jenkins.deb
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

# =====================================================
# УСТАНОВКА GRAFANA (исправлено)
# =====================================================
sudo apt-get install -y software-properties-common
sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
sudo apt update
sudo apt install -y grafana
sudo systemctl start grafana-server
sudo systemctl enable grafana-server

# =====================================================
# УСТАНОВКА KUBECTL
# =====================================================
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo chmod +x kubectl
sudo mv kubectl /usr/local/bin/
kubectl version --client
```
