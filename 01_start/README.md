copy original /ansible configuration in your project:
```
cp -rf /etc/ansible/ mypath/myproject/
```

decomment inventory in file ansible.cfg
from:
```
#inventory      = /etc/ansible/hosts
```

to:
```
inventory      = hosts
```