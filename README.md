# Jenkins install
A simple Ansible role to install a single-node Jenkins server in RHEL/CentOS 7.

## Description
The role will install Jenkins and required packages, open firewall ports and print the initial admin password for the GUI setup. Access to the internet is required.

## Example Playbook
Download role:

    mkdir -p roles; cd roles
    git clone https://github.com/kompjuteras/jenkins_install.git
    cd -

Simple playbook to run this role:

    - name: Jenkins install
      hosts: all
      become: true
      become_user: root
      become_method: sudo
      gather_facts: true
      ignore_errors: false
      roles:
         - jenkins-install

## Author Information
Darko Drazovic \
LinkedIn: https://www.linkedin.com/in/darkodrazovic \
Personal: https://darkodrazovic.in.rs \
Blog: https://kompjuteras.com \
GitHub: https://github.com/darkodrazovic
