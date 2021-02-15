ODBC Driver for MSSQL Server on Ubuntu
=========

Role to enable usage of SQL Server from PHP on Ubuntu

Requirements
------------

None

Role Variables
--------------

None

Dependencies
------------

None

Example Playbook
----------------

   requirements.txt
    # forked to augmesh and updated
    # https://github.com/amestsantim/odbc-driver-for-mssql-on-ubuntu
    # for php
      - src: https://github.com/augmesh/odbc-driver-for-mssql-on-ubuntu
        version: master
        name: odbc-driver-for-mssql-on-ubuntu

   Playbook
    
    - hosts: php
      roles:
         - { role: odbc-driver-for-mssql-on-ubuntu }
   
   Task

    - tasks
    
        - name: role https://github.com/augmesh/odbc-driver-for-mssql-on-ubuntu
          include_role:
            name: odbc-driver-for-mssql-on-ubuntu
          vars:
            mssql_driver_php_version: "{{ php_version }}"
        

License
-------

MIT

Author Information
------------------

I have written up the steps for manual installation in a Medium article which you can find here:
https://medium.com/@nahomt/using-sql-server-from-your-php-apps-on-ubuntu-16-04-c85671249c45
