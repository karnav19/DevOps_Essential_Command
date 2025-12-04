# Ansible Installation & Quickstart (Ubuntu)

## Install
```bash
sudo apt update
sudo apt install -y software-properties-common
sudo add-apt-repository --yes --update ppa:ansible/ansible
sudo apt install -y ansible
ansible --version
```

## Quick test
Create `inventory` file with `localhost ansible_connection=local`
```bash
ansible -i inventory -m ping all
```

## Tips
- Use playbooks for idempotent automation and roles for reusability.
