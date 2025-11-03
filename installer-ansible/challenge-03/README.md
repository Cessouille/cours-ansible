# Challenge 3

- Lancez une VM Rocky Linux et installez Ansible en utilisant PIP et Virtualenv.

```
$ cd ~/formation-ansible/atelier-01
$ vagrant up rocky
$ vagrant ssh rocky
$ sudo dnf install -y epel-release
$ sudo crb enable
$ sudo dnf install -y python3 python3-pip python3-devel
$ python3 -m venv ~/.venv/ansible
$ source ~/.venv/ansible/bin/activate
$ pip install --upgrade pip
$ pip install ansible
$ ansible --version
$ deactivate
$ exit
$ vagrant destroy -f rocky
```
