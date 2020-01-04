### copy rsa key inside server:
if you don't have one create it:
```
ssh-keygen
```

copy inside the server:
```
ssh-copy-id -i ~/.ssh/id_rsa.pub pierangelo@127.0.0.1 -p 2222
```


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

edit hosts:
```

```

after do this try to ping if the servers are connected to ansible:
```
ansible all -m ping
```

or launch a live command:
```
ansible all -a "/bin/echo hello"
```
