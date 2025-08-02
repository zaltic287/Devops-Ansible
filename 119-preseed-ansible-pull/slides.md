

# ANSIBLE : PRESEED > INSTALL ANSIBLE PULL

<br>

Vidéo précédente : ansible push > ansible pull

<br>

* TP

Preseed > ansible push local > ansible pull

<br>

```
d-i preseed/late_command string \
  in-target sh -c "git clone https://Saliou:mtcmVP2BiggViyax_EAD@gitlab.com/Saliou/pre_install_ansible.git /root/preinstall"; \
  in-target sh -c "chmod 755 /root/preinstall/run.sh"; \
  in-target /bin/sh -c "/root/preinstall/run.sh";
```
