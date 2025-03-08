# 🚀test_for_huntflow
---

▶️ [Посмотреть видео DEMO 720p](https://drive.google.com/file/d/1nBMxYcqlcSut2S_RSVHFmPwrQj1Ly5FU/view?usp=sharing)

---
💬 В наличии ноут Apple M1 Pro, виртуалки на vmware использую на arch=arm64
и поимел немного проблем с установкой vmware и установкой плагинов к Vagrant.

⚠️
Для развертывания vm использовал следующую ОС:

```Virtualization: vmware```

```Operating System: Ubuntu 20.04.3 LTS```

```Kernel: Linux 5.4.0-89-generic```

```Architecture: arm64```

### Описание:

Создал vagrant файл с необходимыми параметрами по требованиям указаным в [Тестовом задании](https://github.com/huntflow/devops-test). 

Обновил плагины ansible на локальном mac для docker-compose.

Создал необходимый плейбук для установки необходимых сервисов.

С помощью ansible были произведены настройки необходимых сервисов и приложений.

Были созданы c помощью ansible файлы docker-compose.yml для сборки контейнеров, конфиг prometheus.yml ,dashboard для grafana и настроен datasource в Prometheus.

После запуска, vagrant собирает vm и выполняет настройку vm  c помощью ansible

При переходе по адресу http://localhost:3000 появляется login в Grafana 
```Пользователь: admin ```
```Пароль: admin```

Доступен dashboard `node_exporter` с метриками текущего хоста.
🔥 
<img width="1444" alt="image" src="https://github.com/user-attachments/assets/79ac5e80-f4ec-4821-8615-5b875f14d7eb" />

---



