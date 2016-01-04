Role Name
=========

Nginx setup for django project.

This includes uwsgi and supervisord.

Role Variables
--------------

nginx_port: 80  
nginx_dir: "/etc/nginx"  
nginx_conf_dir: "{{nginx_dir}}/sites-available"  
nginx_sites_dir: "{{nginx_dir}}/sites-enabled"  
nginx_access_log: "/home/{{project_name}}/logs/access.log"  
nginx_error_log: "/home/{{project_name}}/logs/error.log"  

Dependencies
------------

role: dinesh/django_project  

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:  

    - hosts: django-servers  
      remote_user: root
      roles:
        - { role: django_uwsgi_nginx, project_name: 'your_project_name', server_name: domain_name_or_ip_addr }


License
-------

MIT
