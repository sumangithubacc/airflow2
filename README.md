Airflow2 with MSSQL
Airflow2 with mssql. This installs with pre defined airflow2.tar.gz file. if you have an existing setup , please make tar.gz file from airflow home where airflow.cfg, webserver_config.py files exists and copy it under specified location. This should also exist python virtual environment with python version 3.6.

Role name is airflow2
Tasks prereqs ,setup (setting the environment for airflow installation) , install and services
Called by airflow2.yml from base directory with role airflow2
This Creates admin user 'airflow' for WebUI login -> pass is in vars file , also if you are using ldap authentications , it will work as expected
It stops firewalld service and starts webserver services only . You need to start remain services manually as per its(instance) role
It can be customized for prod/syst/test , right now it supplies sandbox(sand) variable from env file ( Please add cfg and webserver files as per type env sand,prod,syst and test like wise shown in templates and files.
Note: 1.Please make sure you have updated airflow.cfg (from files) and webserver_config.py ( templates ) . 2.Make sure you open all required ports like 1433 for mssql ,8080 for webui, ldap..etc to all services part of airflow2 instance. 3.Make sure node has access to redhat repo and mssql redhat repo

REQUIREMENTS: RHEL7 OS with 1G RAM and 2 Core CPU
