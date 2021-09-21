# Install LEMP and Wordpress

## Requirement:
* OS Linux Centos 7
* Python 3.x
* Ansible 2.9

## Variables

1. php_version = PHP Version
2. mariadb_version: Mariadb Version
3. wordpress_version: Wordpress Version
4. user_nginx: User for nginx on PHP Server
5. nginx_config_path = Config path for Nginx
6. nginx_root_folder = Nginx root folder to run Nginx
7. wordpress_config_path = Config path for wordpress
8. nginx_port: Port Nginx
9. php_root_path = PHP root folder to place PHP file
10. php_fpm_port: Port PHP-FPM

## Example hosts inventory file

```
[vms]
nginx ansible_ssh_host=192.168.1.6
mysql ansible_ssh_host=192.168.1.9
php ansible_ssh_host=192.168.1.8

[vms:vars]

ansible_user=root
ansible_password=centos
```