#ansible-docker-ee-ubuntu

##Overview
ansible playbook to install docker EE on ubuntu 16.04

reference: https://docs.docker.com/install/linux/docker-ee/ubuntu/#install-docker-ee

##Content
dockerEE_ubuntu.yml: main playbook 
dockerEE_creds.yml: contains dockerEE-related variables 


##HOWTO

step 1: edit /etc/ansible/hosts with list of ubuntu nodes
step 2: rename dockerEE_creds_sample.yml to dockerEE_creds.yml
step 3: update content of dockerEE_creds.yml with appropriate data

step 4: run the playbook 
ansible-playbook dockerEE_ubuntu.yml --user=ubuntu --private-key=mykey.pem --become

note: "--become" option overlaps with use of task-based become - due to missing become option in apt_key

