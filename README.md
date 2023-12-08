Monitoring-role
=========

Ansible role для установки prometheus, alertmanager и grafana. При выполнении роли автоматически подключается datasource prometheus и создается dashboard Node Exporter Full
Состоит из следующих действий:
- Установка node-exporter - [node-exporter.yml](https://github.com/roman-serdyukov/monitoring-role/blob/main/tasks/node-exporter.yml).
- Установка Docker - [install-docker.yml](https://github.com/roman-serdyukov/monitoring-role/blob/main/tasks/install-docker.yml).
- Настройка и запуск Docker контейнеров - [start-docker.yml](https://github.com/roman-serdyukov/monitoring-role/blob/main/tasks/start-docker.yml).

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
- Учетные данные в папке "vars" 
Учетные данные приведены в папке "vars" только для демонстрации. Рекомендуется хранить в group_vars в защищенном виде

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