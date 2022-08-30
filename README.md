Monitoring-role
=========

Ansible role для установки prometheus, alertmanager и grafana. При выполнении роли автоматически подключается datasource prometheus и создается dashboard Node Exporter Full
Состоит из следующих действий:
- Установка node-exporter.
- Установка Docker install-docker.yml.
- Настройка и запуск Docker контейнеров.

Requirements
------------

Работоспособность протестирована на Ubuntu 20.04.


Role Variables
--------------

В переменных данные:
- Доменное имя.
- Данные для node-exporter (дирректория, версия, адрес скачивания, порт).
- Хосты для мониторинга.
- Порты сервисов.

Example Playbook
----------------
```
- name: Install prometheus/grafana/alertmanager
  hosts: servers
  roles:
    - monitoring-role
```

License
-------

MIT

Author Information
------------------

Сердюков Роман
reserdukov@gmail.com