# Challenge 1

- Démarrez la VM ubuntu depuis le répertoire atelier-01.
`$ cd ~/formation-ansible/atelier-01`
`$ vagrant up ubuntu`

- Connectez-vous à cette VM.
`$ vagrant ssh ubuntu`

- Rafraîchissez les informations sur les paquets.
`$ sudo apt update`

- Recherchez le paquet ansible avec les options qui vont bien.
`$ apt-cache search --names-only ansible`

- Installez le paquet officiel fourni par la distribution.
`$ sudo apt install -y ansible`

- Vérifiez si l'installation s'est bien déroulée.
`$ ansible --version`

- Notez la version d'Ansible.
`$ ansible --version`

- Déconnectez-vous et supprimez la VM.
`$ exit`
`$ vagrant destroy -f ubuntu`
