Jenkins Ansible Role
=========

This role installs jenkins ci server, including configured plugins

Requirements
------------

None

Role Variables
--------------

This role requires the following variables to be defined elsewhere in the playbook that uses it:
```yaml
jenkins_port:          8080
jenkins_home:          /var/lib/jenkins
jenkins_admin_email:   jenkins@golili.net
jenkins_params:
  url_username: admin
  url_password: admin
  url: 'http://localhost: 8080'
jenkins_plugins:        # List of plugins to install
  - ace-editor
  - ant
  - antisamy-markup-formatter
  - authentication-tokens
  - bouncycastle-api
```

Dependencies
------------

This role requires a jdk to be installed before run

Example Playbook
----------------

Register the role in requirements.yml:
```yaml
- src: capitanh.jenkins-ansible-role
  name: jenkins
```
Include it in your playbooks:
```yaml
- hosts: servers
  roles:
    - jenkins
```

License
-------

BSD
