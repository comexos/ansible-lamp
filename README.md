# ansible-lamp
Setup and manage a LAMP system for shared hosting

## Setup Server

To do

## Add Webspace

```bash
ansible-playbook -i <SERVERIP|SERVERFQDN>, web.yml -e 'sys_user=<SYS_USER> web_name=<FQDN> [web_aliases="FQDN1 FQDN2 FQDN3 ..."]' -vv
```

### Optional Parameters
* web_aliases: Additional aliases, separated by spaces
* sys_uid: User id of sys_user
* db_create: Flag to create a database
* srv_admin: Email used in Apache config and for certbot
* web_prefix: Default "/srv/www"
* web_home: Default "{{ web_prefix }}/{{ sys_user }}"
* web_htdocs: Default "{{ web_home }}/htdocs"
* web_logs: Default "{{ web_home }}/logs"
* web_fcgid: Default "{{ web_prefix }}/.fcgid/{{ sys_user }}"
* db_name: Name of db to create
* db_user: Name of db user
* db_password: Password for DB
