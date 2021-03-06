ansible-role-win-fslogix
=========

Installs FSLogix

Role Variables
--------------

The default values for the variables are set in defaults/main.yml:

```yaml
fslogix_extract_dir: 'C:\Windows\Temp\fslogix'
fslogix_download_url: https://download.microsoft.com/download/e/a/1/ea1bcf0a-e66d-48d2-ac9f-e385e5a7456e/FSLogix_Apps_2.9.8171.14983.zip
fslogix_service_product_id: '{8FCB8581-01A9-4563-9D5F-273D4C67ABD2}'
fslogix_rule_editor_product_id: '{35B6888B-7F81-4A52-8262-DE38D617F506}'
fslogix_rule_editor_install: false
fslogix_rule_files_contents: ''
fslogix_no_restart: false
```

Example Playbook
----------------

```yaml
---
- hosts: win10
  become: true
  gather_facts: true
  vars:
    fslogix_rule_editor_install: true

  roles:
    - ansible-role-win-fslogix
```
