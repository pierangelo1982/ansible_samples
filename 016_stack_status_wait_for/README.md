con lineinfile, utilizziamo REGEXP per trovare la linea e modificarla, senza dover caricare un appoosito template .j2

```
lineinfile:
        dest: /etc/mysql/my.cnf
        regexp: ^bind-address line="bind-address = 0.0.0.0" # sovrascrive 127.0.0.1 in my.cnf
```