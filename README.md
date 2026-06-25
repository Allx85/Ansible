# Ansible


Bygga om allt
`docker compose up -d --build`

Pingar myhosts i guppen i inventory
`ansible myhosts -m ping -i inventory.ini`

Tvingar ssh-agent att validera
```eval $(ssh-agent)
ssh-add /root/.ssh/id_ed25519```

För att komma ur neovim
`:q` 

Installera program i containrarna med playbook
 `ansible-playbook install_packages.yaml -i inventory.ini`