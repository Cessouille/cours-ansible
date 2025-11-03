# Challenge

- Placez-vous dans le répertoire du troisième atelier pratique.  
`$ cd ~/formation-ansible/atelier-03`

- Voici les quatre machines virtuelles Ubuntu 22.04 de cet atelier.  
| Machine virtuelle  | Adresse IP     |
|--------------------|----------------|
| control            | 192.168.56.10  |
| target01           | 192.168.56.20  |
| target02           | 192.168.56.30  |
| target03           | 192.168.56.40  |

- Démarrez les VM.  
`$ vagrant up`

- Connectez-vous au *Control Host*.  
`$ vagrant ssh control`

- Ansible est déjà installé sur cette machine.  
`$ type ansible`

