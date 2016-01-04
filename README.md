Role Name
=========

Nginx setup for django project.

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
      roles:  
         - { role: dinesh.django_nginx }  

License
-------

MIT
