# Challenge 3

- Démarrez la VM `rocky` depuis le répertoire `atelier-01`.

```sh
cd ~/formation-ansible/atelier-01
vagrant up rocky
```

- Connectez-vous à cette VM.

```sh
vagrant ssh rocky
```

- Installez Ansible en utilisant PIP et Virtualenv.

```sh
sudo dnf install -y epel-release
sudo crb enable
sudo dnf install -y python3 python3-pip python3-devel
python3 -m venv ~/.venv/ansible
source ~/.venv/ansible/bin/activate
pip install --upgrade pip
pip install ansible
ansible --version
deactivate
```

- Déconnectez-vous et supprimez la VM.

```sh
exit
vagrant destroy -f rocky
```
