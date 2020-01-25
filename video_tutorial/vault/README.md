### VAULT

how encrypt and secure passwords ecc...

# 1
in cartella group_vars crea cartella all...
In all crea file vars con variabili
sempre in all lancia comando:
```
ansible-vault create vault
```
automaticamente crea un file temporaneo nel quale inserire variabile con password che poi verrà criptata nel file vault:
```
---
vault_db_pass: demo

```

per modificarla:
```
ansible-vault edit vault
```

ora che password è criptata se lanci ansible darà errore perchè è necessario passare chiave per decryptarla:

ci son due modi:
modo 1, probabilmente il più scomodo:
```
ansible-playbook database.yml --ask-vault-pass
```

modo 2 - creare file locale:
da quale parte crea un file con la chiave di decriptazione, nel mio caso la metto in root computer, se invece la metti nel progetto in repo metti in .gitignore.
N.B: non la password del db, ma quella messa per cryptare file vault 
```
echo "miapasswordfile" > ~/.vault_pass.txt
```

in ansible.cfg edit:
```
vault_password_file = ~/.vault_pass.txt
```

