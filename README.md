## Role Bamboo Notifications
=========

[![Build Status](https://travis-ci.org/oherrerav/bamboo_notifications.svg?branch=master)]
(https://travis-ci.org/oherrerav/bamboo_notifications)

This role is used for send customs notifications for deployments in Bamboo.

## Requirements
------------
Ansible 2.4.2.0

## Role Variables
--------------
Here is a list of all the default variables for this role, which are also available in defaults/main.yml. 
``` yml
---
bamboo_appUrl: >-
   http://{bamboo}/deploy/viewDeploymentResult.action?deploymentResultId={id}
bamboo_deploy_environment: Development
bamboo_deploy_previous_release: v0.0.0
bamboo_deploy_project: Admeasurement
bamboo_deploy_release: develop
bamboo_deploy_rollback: 'true'
bamboo_resultsUrl: >-
  http://{bamboo}:8085/deploy/viewDeploymentResult.action?deploymentResultId={id}
teams_webhook: >-
  https://outlook.office.xxxxx
AZURE_AD_USER: user
AZURE_PASSWORD: password
```
## Dependencies
------------

No depencies

## Example Playbook
----------------

And here's the playbook:

``` yml
---
- name: Bamboo Notifications
  hosts: all
  connection: local
  gather_facts: no
  any_errors_fatal: True
  tasks:
  - name: Include role bamboo_notifications
    include_role:
      name: ../roles/bamboo_notifications
```
## License
-------

BSD

## Author Information
------------------

OAHerrera