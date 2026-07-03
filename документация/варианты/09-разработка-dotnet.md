# Вариант 9: .NET разработка

> Команды собраны из исходного материала без проверки на конкретной версии Ubuntu. Версии пакетов, ссылки и доступность Snap могут меняться.

```bash
# =====================================================
# УСТАНОВКА VS CODE
# =====================================================
sudo snap install --classic code

# =====================================================
# УСТАНОВКА .NET SDK (исправлено)
# =====================================================
wget -O dotnet-install.sh https://dot.net/v1/dotnet-install.sh
chmod +x dotnet-install.sh
./dotnet-install.sh --channel 8.0
echo 'export PATH="$HOME/.dotnet:$PATH"' >> ~/.bashrc
source ~/.bashrc
dotnet --version

# =====================================================
# УСТАНОВКА MS SQL SERVER
# =====================================================
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/22.04/prod.list)"
sudo apt update
sudo apt install -y mssql-server
sudo /opt/mssql/bin/mssql-conf setup

# =====================================================
# УСТАНОВКА DOCKER
# =====================================================
sudo apt install -y docker.io
sudo systemctl start docker
sudo usermod -aG docker $USER
```
