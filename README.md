yti-redbot
=========

An Ansible role to automatically create Discord bots based on Redbot.  
In addition to creating bots, repos and cogs can also be installed and loaded automatically

No frickling with ***I agree*** anymore


Requirements
------------

None

Role Variables
--------------

Defaults:  
data_path: /srv/redbot => Directory where bots are stored

Example Configuration

```
redbot:
  - name: Bot1
    settings:
      prefix: b!
      token: 123456789
      state: started 
      onboot: true
    repos:
      - name: local
        cogs:
          - admin
          - downloader
          - audio
      - name: zeacogs
        url: https://github.com/ZeLarpMaster/ZeCogsV3.git
        cogs:
          - react_roles
```

Dependencies
------------

None

