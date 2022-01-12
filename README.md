ansible-role-win-fslogix
=========

Installs FSLogix

Role Variables
--------------

The default values for the variables are set in defaults/main.yml:

```yaml
fslogix_extract_dir: 'C:\Windows\Temp\fslogix'
fslogix_download_url: https://aka.ms/fslogix_download
fslogix_service_product_id: '{11A79880-FCDA-4252-BE28-BF7D1C38FBE9}'
fslogix_rule_editor_product_id: '{53C83608-DF84-41DA-B658-A03F548EF522}'
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
