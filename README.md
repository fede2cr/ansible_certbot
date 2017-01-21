# ansible_certbot [![Build Status](https://travis-ci.org/fede2cr/ansible_certbot.svg?branch=master)](https://travis-ci.org/fede2cr/ansible_certbot)

Ansible recipes for certbot for easy install and admin of Let's Encrypt

## Instructions
1. Create inside the recipe folder, an ```inventory/``` folder with a ```hosts``` file inside with a content like:

```
10.1.2.3 ansible_user=alvaro
```
2. ```ssh-copy-id``` to the server
3. Either create a ```sudo``` file to avoid writing the password, or add ```-K``` to ```ansible-playbook```
4. Run ansible-playbook inside the recipe dir
```
ansible-playbook some-recipe.yml
```

If you don't want to create an inventory you can use an example file:
```
ansible-playbook certbot_install.yml -i ../inventory/hosts.example -K
```
