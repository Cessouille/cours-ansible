# Challenge 1

- Démarrez la VM ubuntu depuis le répertoire atelier-01.

```sh
cd ~/formation-ansible/atelier-01
vagrant up ubuntu
```

- Connectez-vous à cette VM.

```sh
vagrant ssh ubuntu
```

- Rafraîchissez les informations sur les paquets.

```sh
sudo apt update
```

- Recherchez le paquet ansible avec les options qui vont bien.

```sh
apt-cache search --names-only ansible
```

- Installez le paquet officiel fourni par la distribution.

```sh
sudo apt install -y ansible
```

- Vérifiez si l'installation s'est bien déroulée.

```sh
ansible --version
```

- Notez la version d'Ansible.

```sh
ansible --version
```

- Déconnectez-vous et supprimez la VM.

```sh
exit
vagrant destroy -f ubuntu
```
