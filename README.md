npm
=========

Nginx Proxy Manager (npm) is a docker image that enables you to easily forward to your websites running at home or otherwise, including free SSL, without having to know too much about Nginx or Letsencrypt.

This Ansible role installs npm as a Docker service.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):


```
npm_ui_image: "jc21/nginx-proxy-manager:latest"
```
The version of the docker image to run as a container.

```
npm_db_image: "jc21/mariadb-aria:latest"
```
Database docker image version

```
npm_db_user: "nginx_proxy_manager"
```
Database user

```
npm_db_password: "nginx_proxy_manager"
```
Database password

```
npm_db_root_password: "r00t!"
```
Database root password

```
npm_db_name: "nginx_proxy_manager"
```
Database name

```
npm_ui_host_http_port: 80
```
npm http host port

```
npm_ui_host_http_port: 81
```
npm admin host port

```
npm_ui_host_https_port: 443
```
npm https host port

```
npm_host_config_path: /etc/nginx_proxy_manager
```
Host path which stores npm configuration.

```
npm_host_letsencrypt_path: /var/lib/nginx_proxy_manager/letsencrypt

```
Host path which stores letsencrypt data.

```
npm_host_data_path: /var/lib/nginx_proxy_manager/data

```
Host path which stores npm data.

```
npm_host_db_path: /var/lib/nginx_proxy_manager/mysql/data
```
Host path which stores npm database.

```
npm_container_user: nginx_proxy_manager
```
user running the container 

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - iasensio.nginx_proxy_manager

License
-------

MIT

