MONGO
=========

通过 ansible 部署在容器下运行的 Mongo 服务。

Installation
------------

`ansible-galaxy install gengxiankun.mongo`

Role Variables
--------------

variable | description
------------ | -------------
OPT_PATH | 部署目录
SRV_PATH | 服务运行时持久化目录
MONGO_PORT | mongo 服务对外监听端口
MONGO_EXPRESS_PORT | mongo express 服务对外端口
MONGO_INITDB_ROOT_USERNAME | mongo 用户名
MONGO_INITDB_ROOT_PASSWORD | mongo 密码
MONGO_EXPRESS_ENABLE | 是否启用 mongo express

Dependencies
------------

- docker

Example Playbook
----------------

    - hosts: servers
      roles:
        - gengxiankun.mongo
      vars:
        - OPT_PATH: /opt
        - SRV_PATH: /data/runtime
        - MONGO_PORT: 27017
        - MONGO_EXPRESS_PORT: 28081
        - MONGO_INITDB_ROOT_USERNAME: root
        - MONGO_INITDB_ROOT_PASSWORD: root
        - MONGO_EXPRESS_ENABLE: true

License
-------

BSD

Author Information
------------------

This role was created in 2019 by Xiankun Geng, Learn more about the author's role in [galaxy](https://galaxy.ansible.com/gengxiankun).
