# Ansible

## Installation
Installation från [Ansible](https://docs.ansible.com/projects/ansible/latest/getting_started/index.html)

## Utförande
Vi byggde upp två containrar med docker som var våra managed nodes. Host datorn var Control node.

## Lärdommar
Att skapa ssh-nycklar och kopiera över dem i containrarna.
Vi fick bygga om många gånger under labben. Viktigt kommando att komma ihåg i docker.
`docker compose up -d --build`

Tvingar ssh-agent att validera vald nyckel
`eval $(ssh-agent)
ssh-add /root/.ssh/id_ed25519`

Vi testade att installera neovim med playbook och då var det viktigt att komma ur neovim med kommandot:`:q` 

## Kommandon


Pingar myhosts i guppen i inventory
`ansible myhosts -m ping -i inventory.ini`

Installera program i containrarna med playbook
 `ansible-playbook install_packages.yaml -i inventory.ini`