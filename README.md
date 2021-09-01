Code Objective
--------------
- Code to make it easier to automate Cisco vulnerabilities checks for Network devices.

Design
--------
- Code split into 5 main steps.
  * Step 1 : Ansible ios_facts in-built module, obtain {{ ansible_net_version }} and {{ ansible_net_iostype }}.
  * Step 2 : Ansible uri in-built module, obtain Cisco PISRT API token.
  * Step 3 : Ansible uri in-built module, do API call to cisco software checker.
  * Step 4 : Ansible file in-built module, create a {{ ansible_net_hostname }}_vulnerabilities.txt file.
  * Step 5 : Ansible lineinfile in-built module ,write chosen fields to a file in step 4.

Playbooks 
---------
- main.yml  : Main playbook
- collect_vars.yml : Step 1 tasks
- vulnerabilities_checks.yml : Step 2 and Step 3 tasks
- write_to_file.yml : Step 4 and Step 5 tasks

Definitions
-----------
- PISRT : Product Security Incident Response Team
- API : Application Programming Interface

Code Authors
------------
- Allan Maseghe 
