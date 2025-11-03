# Challenge 2

- Démarrez la VM ubuntu depuis le répertoire atelier-01.

```
$ cd ~/formation-ansible/atelier-01
$ vagrant up ubuntu
```

- Connectez-vous à cette VM.

```
$ vagrant ssh ubuntu
```

- Configurez un dépôt PPA (Personal Package Archive) pour Ansible

```
$ sudo apt-add-repository ppa:ansible/ansible
```

- Rafraîchissez les informations sur les paquets.

```
$ sudo apt update
```

- Recherchez le paquet ansible avec les options qui vont bien.

```
$ apt-cache search --names-only ansible
```

- Installez le paquet officiel fourni par la distribution.

```
$ sudo apt install -y ansible
```

- Vérifiez si l'installation s'est bien déroulée.

```
$ ansible --version
```

- Notez la version d'Ansible.

```
$ ansible --version
```

- Déconnectez-vous et supprimez la VM.

```
$ exit
$ vagrant destroy -f ubuntu
```

## Version
> ansible [core 2.17.14]  
  config file = /etc/ansible/ansible.cfg  
  configured module search path = ['/home/vagrant/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']  
  ansible python module location = /usr/lib/python3/dist-packages/ansible  
  ansible collection location = /home/vagrant/.ansible/collections:/usr/share/ansible/collections  
  executable location = /usr/bin/ansible  
  python version = 3.10.12 (main, Aug 15 2025, 14:32:43) [GCC 11.4.0] (/usr/bin/python3)  
  jinja version = 3.0.3  
  libyaml = True
