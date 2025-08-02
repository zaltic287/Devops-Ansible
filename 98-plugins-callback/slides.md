

# ANSIBLE : LES PLUGINS CALLBACK

<br>

Documentation :
https://docs.ansible.com/ansible/2.9/plugins/callback.html

```
ansible-doc -t strategy -l
```

<br>

* DELAY : profile_tasks

Doc : https://docs.ansible.com/ansible/latest/collections/ansible/posix/profile_tasks_callback.html

```
[defaults]
callback_whitelist = profile_tasks
```

<br>

* OUTPUT : yaml 

Doc : 

```
[defaults]
stdout_callback = yaml
bin_ansible_callbacks = True
```

----------------------------------------------------------------------------------------------

# ANSIBLE : LES PLUGINS CALLBACK


<br>

* OUTPUT : filtre

Doc : https://docs.ansible.com/ansible/2.9/plugins/callback/default.html

```
[defaults]
display_ok_hosts = no
```

<br>

* CHOISIR : selective

Doc : https://docs.ansible.com/ansible/2.9/plugins/callback/selective.html

```
[defaults]
stdout_callback: selective
```

Et taguer les tasks :

```
    tags: [print_action]
```
