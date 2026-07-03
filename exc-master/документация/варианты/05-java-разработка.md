# Вариант 5: Java-разработка

> Команды собраны из исходного материала без проверки на конкретной версии Ubuntu. Версии пакетов, ссылки и доступность Snap могут меняться.

```bash
# =====================================================
# УСТАНОВКА INTELLIJ IDEA
# =====================================================
sudo snap install intellij-idea-community --classic

# =====================================================
# УСТАНОВКА JDK
# =====================================================
sudo apt install -y openjdk-17-jdk openjdk-17-jre
java -version
javac -version

# =====================================================
# УСТАНОВКА MAVEN
# =====================================================
sudo apt install -y maven
mvn -version

# =====================================================
# УСТАНОВКА TOMCAT (исправлено)
# =====================================================
wget -O tomcat.tar.gz https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.28/bin/apache-tomcat-10.1.28.tar.gz
sudo tar -xf tomcat.tar.gz -C /opt
sudo chmod +x /opt/apache-tomcat-10.1.28/bin/*.sh
/opt/apache-tomcat-10.1.28/bin/startup.sh
# Открыть в браузере: http://localhost:8080
```
