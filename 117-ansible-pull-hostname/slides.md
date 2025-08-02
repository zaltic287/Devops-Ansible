

# ANSIBLE : PULL - HOSTNAME ET VAULT

<br>

* travailler avec un inventaire

```
all:
  children:
    grp1:
      hosts:
        ans1:
```

<br>

```
ansible-pull -U git@gitlab.com:Saliou/my_ansible_pull.git --private-key /home/vagrant/.ssh/id_rsa --accept-host-key -i "ans1,"
```

```
ansible-pull -U git@gitlab.com:Saliou/my_ansible_pull.git --private-key /home/vagrant/.ssh/id_rsa --accept-host-key -i "$(hostname)"
```

-----------------------------------------------------------------------------------------


# ANSIBLE : PULL - HOSTNAME, VAULT ET LIMITES


<br>

* sur le dépôt ? OUI

<br>

* sur le host ? OUI

=> grosse contrainte

par exemple :

```
/etc/ansible/inventory.yml
-i /etc/ansible/inventory.yml
```

<br>

* idem pour les variables vaultées

```
--vault-password-file /root/.vault
```
