# npmE Ansible

npmE Ansible installs OS-specific dependencies for npm Enteprise:

* Nginx.
* CouchDB.
* Redis.
* Node.js.

# Usage

npmE Ansible helps you get npm up and running on a blank Ubuntu (or Debian) image.

Simply follow these instructions (_even if you've never used Ansible before, it's easy!_):

1. Install [Ansible](http://docs.ansible.com/intro_installation.html) on your development machine.
2. Install [Ansible-Librarian](https://github.com/bcoe/librarian-ansible) on your development machine.
3. Create an Ansible project with the following `Ansiblefile`:

```yml
# Node.js
role "laggyluke.nodejs"

# npmE
role "bcoe.npme"
```
4. Create a new directory to use for your Ansible deployments.
5. Copy the example `deploy.yml`, `Ansiblefile`, `ansible.cfg`, and `inventory` to this directory.
6. Run: `ansible-librarian install` to install Ansible dependencies.
7. Create a blank Ubuntu image.
8. Update `inventory` to point to the blank Ubuntu image.
9. Run: `ansible-playbook ./deploy.yml -i inventory`.

That's all there is to it! patches welcome.
