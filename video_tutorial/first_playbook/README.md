comandi esempi ecc.. per selezionare l'HOST

```
ansible all -m ping

ansible development -m ping

ansible \!development -m ping

ansible 192.168.* -m ping

ansible --list-hosts all

ansible --list-hosts development

ansible --list-hosts \!development
```