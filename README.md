CentOS 7 All in One WebServer Install
=========

Install basic packages and update OS, install Nginx on latest version, PHP 7.2/PHP 7.3/PHP 7.4 with specific modules and MySQL Community Server 5.6.49.

Requirements
------------

1. Allow Ansible Server communicate to new instante, executing the command `ssh-copy-id root@IPVIRTUALMACHINE`;
2. Add the IPVIRTUALMACHINE on `/etc/ansible/hosts` file;
3. Insert the IPVIRTUALMACHINE on file main.yml and choose wich are roles do you execute; 
4. Execute the playbook `main.yml`;
And Voalá...

**OBS 1**: The MySQL root password is on the directory vars, `roles/mysqld/vars/`.</br>
**OBS 2**: The WebServer Username is defined on `roles/usrdev/vars/main.yml`.</br>


Example executing playbook with file main.yml
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
Uncoment role line to install one or more packages, choose one version of PHP.


```sh
---
- name: Apply common configuration on webserver instance
  hosts: IPVIRTUALMACHINE
  gather_facts: no
  ignore_errors: yes

  roles:
#    - { role: packages }
#    - { role: nginx }
#    - { role: php7.2 }
#    - { role: php7.3 }
#    - { role: php7.4 }
#    - { role: vsftpd }
#    - { role: usrdev }
#    - { role: mysqld }

```

License
-------

Use where you think you will contribute :)

Author Information
------------------

* **Joel Pinheiro** - *Github* - [joelcpinheiro](https://github.com/joelcpinheiro)


