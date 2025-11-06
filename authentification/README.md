# À vous de jouer !

- Placez-vous dans le répertoire du troisième atelier pratique.

```
$ cd ~/formation-ansible/atelier-03
```

- Voici les quatre machines virtuelles Ubuntu 22.04 de cet atelier.

  | Machine virtuelle | Adresse IP     |
  | :---------------- | :------------- |
  | control           | 192.168.56.10  |
  | target01          | 192.168.56.20  |
  | target02          | 192.168.56.30  |
  | target03          | 192.168.56.40  |

- Démarrez les VM.

```
$ vagrant up
```

- Connectez-vous au *Control Host*.

```
$ vagrant ssh control
```

- Ansible est déjà installé sur cette machine.

```
$ type ansible
```

- Ajoutez les adresses et les noms d'hôtes au *Control Host*.

```
$ sudo nano /etc/hosts
```

```
192.168.56.10   ansible.sandbox.lan     control
192.168.56.20   target01.sandbox.lan    target01
192.168.56.30   target02.sandbox.lan    target02
192.168.56.40   target03.sandbox.lan    target03
```

- Testez l'authentification sur les *Target Hosts*

```
$ ansible all -i target01,target02,target03 -m ping
```

Les connexions échouent.
![Capture d'écran des connexions échouant](ssh_ping_error.png)

- Testez la connectivité aux machines.

```
$ for HOST in target01 target02 target03; do ping -c 1 -q $HOST; done
```

Les pings réussissent.
![Capture d'écran des pings réussissant](ping_success.png)

- Collectez les clés SSH publiques des *Target Hosts*.

```
$ ssh-keyscan -t rsa target01 target02 target03 >> .ssh/known_hosts
```

- Testez les connexions ssh.

```
$ ssh target01
$ ssh target02
$ ssh target03
```

Les 3 connexions fonctionnent.

- Générez une paire de clés SSH.

```
$ ssh-keygen
```

![Capture d'écran de la génération de la paire de clés SSH](ssh-keygen.png)

- Distribuez la clé publique aux *Target Hosts*.

```
$ ssh-copy-id vagrant@target01
$ ssh-copy-id vagrant@target02
$ ssh-copy-id vagrant@target03
```

![Capture d'écran de la distribution de la clé publique](ssh-copy-id.png)

- Testez de nouveau l'authentification sur les *Target Hosts*

```
$ ansible all -i target01,target02,target03 -m ping
```

Les connexions réussissent.
![Capture d'écran des connexions réussissant](ssh_ping_success.png)
