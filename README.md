## Shell commands
============================
### ![Bash Script](https://img.shields.io/badge/bash_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)

### 1. Увеличение времени таймаута SSH соединения в Linux

Здесь находится конфигурационный файл для ssh

`sudo nano /etc/ssh/sshd_config`

> **ClientAliveInterval** Задает интервал (в секундах), с которым сервер SSH отправляет клиенту сообщение keepalive (сигнал, отправляемый для проверки активности клиента

> **ClientAliveCountMax** Определяет количество keepalive-сообщений, которые могут быть отправлены клиенту без получения ответа

Общее время таймаута SSH-соединения определяется такой формулой

**Timeout time = ClientAliveInterval * ClientAliveCountMax**

После изменения настроека необходимо перезагрузить служку `ssh`:

`sudo systemctl reload sshd`

### 2. Еще команды