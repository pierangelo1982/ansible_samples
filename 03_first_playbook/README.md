### first playbook

# create a task:

create a folder named playbooks:

in playbook folder create a foile with the name of the task that you want:
in my case hotname.yml
```
---
  - hosts: production
    tasks:
      - name: mostra hostname del server
        command: hostname
```

launch ansible command:
```
ansible-playbook playbooks/hostname.yml
```