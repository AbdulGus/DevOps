# Практическая работа по Ansible

В репозитории собраны пять учебных playbook и их подробный разбор. Работа охватывает установку Nginx, создание пользователя, обновление пакетов, резервное копирование конфигурации и управление Docker-контейнерами.

## Состав репозитория

- [`ansible-playbooks/REPORT.md`](ansible-playbooks/REPORT.md) — письменный разбор всех сценариев;
- [`ansible-playbooks/01-nginx.yml`](ansible-playbooks/01-nginx.yml) — установка и настройка Nginx;
- [`ansible-playbooks/02-create-user.yml`](ansible-playbooks/02-create-user.yml) — создание пользователя `newadmin`;
- [`ansible-playbooks/03-update-packages.yml`](ansible-playbooks/03-update-packages.yml) — обновление пакетов и перезагрузка;
- [`ansible-playbooks/04-backup-configs.yml`](ansible-playbooks/04-backup-configs.yml) — резервное копирование конфигурационных файлов;
- [`ansible-playbooks/05-docker-containers.yml`](ansible-playbooks/05-docker-containers.yml) — установка Docker и создание контейнеров.

## Запуск

Для запуска нужен inventory-файл, в котором определены группы `NGINX` и `ubuntu_vm`. Пример команды:

```bash
ansible-playbook -i inventory.ini ansible-playbooks/01-nginx.yml
```

Перед применением на реальном сервере необходимо заменить тестовые пароли, адреса и имена пользователей своими значениями.
