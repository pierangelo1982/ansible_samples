###

using
gather_facts: false

remove gather_facts where not used.


aggiungendolo aggiorniamo apt solo ogni tot tempo.
```
tasks:
    - name: update apt cache
      apt: update_cache=yes cache_valid_time=86400

```