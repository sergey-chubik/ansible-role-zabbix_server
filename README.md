Ansible Role: Zabbix Server
=========

Эта роль установит Zabbix сервер версии 5.0 с базой данных PostgreSQL и расширением TimescaleDB на CentOS 7.

Requirements
------------

None.

Role Variables
--------------

Доступные переменные перечислены ниже вместе со значениями по умолчанию (см. `defaults/main.yml`).
Незабудте указать свои настройки пользователя базы данных zabbix:
  - zabbix_server_db_user: zabbix
  - zabbix_server_db_password: zabbix

Dependencies
------------

Также необходимо открыть следующие службы и порты в firewall
  - service: http
  - port: 10050-10051/tcp
  - port: 161-162/udp

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - zabbix_server

License
-------

BSD

Author Information
------------------

Chubik Sergey, chubik@ekaterinburg.fsin.uis.
