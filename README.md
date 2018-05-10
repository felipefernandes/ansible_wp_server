# Ansible: Wordpress + Apache + MySQL + PHP - INFRA

## Pre-requisites

 - You will need [Ansible](http://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed in your local machine 
 - You will need the SSH Private Key file to access your server

## Before Start

Create a `hosts` file adding the correct IP/Host of your server and the path of your SSH Private Key, place this file on root level.

Your file will looke like this:

```
[production]
192.168.1.10 ansible_user=root ansible_ssh_private_key_file="/users/macbookair/.ssh/myprivatesshkey"
```

Remember:
`192.168.1.10` - is the remote IP/Host address of your server
`/users/macbookair/.ssh/myprivatesshkey` - is the full path of your private key localled at your machine.

### Environment Setup

You won't need to update anything more unless you would like to provide this stack to another envirionment, like a Review server. Therefore you can check and update the file `all.yml` inside *group_vars* folder, changing the values to informations of your project.


## Let's rock!

To provisioning the infrastructure you will just need to run the `run.sh` script and let ansible will do its work.

So, the Ansible will be resposible to:

	1. Install OS Dependences (e.g. Apache2, PHP, Modules for Apache, PHP and MySQL)
	2. Download the latest version of Wordpress
	3. Uncompress the Wordpress in a temp folder and copy the result to the right place
	4. Create and setup the wp-config file
	5. (bonus) Create a theme folder



