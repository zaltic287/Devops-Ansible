

# ANSIBLE : Register - Stat


<br>

Documentation : https://docs.ansible.com/ansible/latest/modules/stat_module.html

Paramètres :

* path : chemin du fichier ou répertoire

* follow : suivre les liens symboliques

* get_checksum  : récupérer la checksum

* checksum_algorithm : type de checksum (md5, etc)

* get_mime: récupération du type de données 

--------------------------------------------------------------

# ANSIBLE : Register - Stat


<br>

* création d'un fichier

```
  - name: création d'un fichier
    file:
      path: /tmp/Saliou.txt
      state: touch
      owner: Saliou
```

<br>

* utilisation de stat

```
  - name: check avec stat
    stat:
      path: /tmp/Saliou.txt
```

<br>

* récupération de la variable

```
  - name: check avec stat
    stat:
      path: /tmp/Saliou.txt
    register: __fichier_xavki_exist
  - name: debug
    debug:
      var: __fichier_xavki
```

--------------------------------------------------------------

# ANSIBLE : Register - Stat


<br>

* récupération d'une clef

```
  - name: debug
    debug:
      var: __fichier_xavki.stat.exists
```

<br>

* utilisation conditionnnel

```
  - name: création répertoire Saliou
    file:
      path: /tmp/Saliou
      state: directory
    when: __fichier_xavki.stat.exists
```

<br>

* exemple: 

```
  tasks:
  - name: création d'un fichier
    file:
      path: /tmp/Saliou.txt
      state: touch
      owner: root
    when: xavki_file is defined
  - name: check avec stat
    stat:
      path: /tmp/Saliou.txt
    register: __fichier_xavki
  - name: debug
    debug:
      var: __fichier_xavki.stat.exists
  - name: création répertoire Saliou
    file:
      path: /tmp/Saliou
      state: directory
    when: __fichier_xavki.stat.exists and xavki_file is defined
```
