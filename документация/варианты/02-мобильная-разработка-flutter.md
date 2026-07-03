# Вариант 2: Мобильные приложения (Flutter/Dart)

> Команды собраны из исходного материала без проверки на конкретной версии Ubuntu. Версии пакетов, ссылки и доступность Snap могут меняться.

```bash
# =====================================================
# УСТАНОВКА VS CODE
# =====================================================
sudo snap install --classic code

# =====================================================
# УСТАНОВКА FLUTTER (исправлено - рабочая версия)
# =====================================================
cd ~
wget -O flutter.tar.xz https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.24.0-stable.tar.xz
tar -xf flutter.tar.xz
export PATH="$PATH:$HOME/flutter/bin"
echo 'export PATH="$PATH:$HOME/flutter/bin"' >> ~/.bashrc
source ~/.bashrc
flutter doctor

# =====================================================
# УСТАНОВКА ANDROID STUDIO
# =====================================================
sudo snap install android-studio --classic

# =====================================================
# УСТАНОВКА GIT
# =====================================================
sudo apt install -y git

# =====================================================
# УСТАНОВКА ПЛАГИНОВ VS CODE ДЛЯ FLUTTER
# =====================================================
code --install-extension Dart-Code.dart-code
code --install-extension Dart-Code.flutter
```
