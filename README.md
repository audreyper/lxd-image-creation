# Ansible Playbook: Create Image of a LXD Container

This Ansible playbook automates the process of creating a LXD container and publishing it as an image.

## Prerequisites

Before running this playbook, ensure you have the following prerequisites set up:

### 1. Ansible installed 

### 2. Inventory File: 

If you won't use localhost as the host, create an inventory.ini file with the necessary host configurations. Refer to the Ansible documentation for more information on creating an inventory file.

### 3. Ansible Configuration: 

You may need to set up an ansible.cfg file with the following configurations:

- host_key_checking 
- ansible_ssh_private_key_file 
- remote_user 

Adjust these configurations based on your environment and requirements.

### 4. Variables File: 

Set up a variables.yaml file with the following variables:

- new_container: Name of the new LXD container.
- image_alias: Alias for the published LXD container image.
- username1: Name of first user created.
- username2: Name of second user created.
- user2_pass: Password of second user.


### Usage

To use this playbook, follow these steps:

1. Ensure you have met all the prerequisites mentioned above.

2. Clone this repository to your local machine:

`git clone https://github.com/audreyper/lxd-image-creation`

Navigate to the directory containing the playbook:

`cd <playbook-directory>`

Run the playbook:

`ansible-playbook playbook.yml -i inventory.ini`