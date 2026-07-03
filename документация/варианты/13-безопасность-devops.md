# Вариант 13: DevSecOps (SAST/DAST/SCA)

> Команды собраны из исходного материала без проверки на конкретной версии Ubuntu. Версии пакетов, ссылки и доступность Snap могут меняться.

```bash
# =====================================================
# УСТАНОВКА JENKINS
# =====================================================
sudo apt install -y openjdk-17-jdk
wget -O jenkins.deb https://get.jenkins.io/debian-stable/jenkins_2.452.2_all.deb
sudo dpkg -i jenkins.deb 2>/dev/null || sudo apt --fix-broken install -y
sudo dpkg -i jenkins.deb
sudo systemctl start jenkins

# =====================================================
# УСТАНОВКА SONARQUBE (исправлено)
# =====================================================
wget -O sonarqube.zip https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-10.6.0.92116.zip
sudo unzip sonarqube.zip -d /opt
/opt/sonarqube-10.6.0.92116/bin/linux-x86-64/sonar.sh start

# =====================================================
# УСТАНОВКА TRIVY
# =====================================================
sudo apt install -y trivy
```
