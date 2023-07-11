---
sidebar_position: 2
---

# Set Up NPLD8 on a Staff PC

Set up a staff computer so staff person can work on NPL Drupal site. Local development environment is based on DrupalVM.

See video from setting up Cook and Ellis local development environments on Z: [need to link on onedrive](Aten Training_2020-07-13_D8-Project-X-Setting-up-with-DrupalVM-Vagrant-Ansible_fixing-cook-ellis-macs)

GET HELP FROM COOK LINKING

## Requirements

Below is an overview of requirements and how they're used. Download by following the instructions in the next section because some tools need to be installed in a certain order.

- **Composer**: Tool for dependency management in PHP. Drupal 8+ requires Composer.
- **VirtualBox**: Tool to create a VM where you can run a different operating system within your own computer. We're using VirtualBox for local development to mimic the environment that we have on Pantheon so that we're developing on the same stack we have remotely.
- **Vagrant**: Tool that wraps around VirtualBox that allows you to automate configuration of a VM. Configurations are stored in a Vagrantfile. Running `vagrant up` triggers the installation of all the configurations outlined in the Vagrantfile which ensures that multiple developers will all be using the same environment. By using both VirtualBox and Vagrant, you can simulate the production environment on Pantheon (or whoever hosts the live site).
- **Ansible**: Tool that wraps around Vagrant that allows you to automate the installation of configurations stored in a "playbook." Vangrant runs the playbook you've written once the VM is booted up.
- **Project-X**: Tool that wraps around Vagrant that manages the whole Drupal project (bringing up the environment, moving things along with tickets, installing Drupal, managing things within Drupal, etc.). If we change development environments, we'll update settings and none of the commands we use will have to change.
- **PHP 7.2** (or higher)

## Download and Install Software

1. Download and Install Composer:
   1. Download at [getcomposer.org/download](https://getcomposer.org/download)
   1. Install following prompts.

1. Download and Install VirtualBox:
   1. Download at [virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
   1. Install following prompts. We install this first because Vagrant may have a dependency on VirtualBox.

1. Download and Install Vagrant:
   1. Download at [vagrantup.com/downloads](https://www.vagrantup.com/downloads)
   1. Install following prompts.

1. Download and Install Ansible:
   1. Download at[docs.ansible.com/ansible/latest/user_guide/windows_usage.html ](https://docs.ansible.com/ansible/latest/user_guide/windows_usage.html)
   1. Install following prompts.

## Set Up the Local Development Site with Project-X
