# Install AWX on RHEL 7

## Pre-Requisites:
1. Enable RedHat Repository for ansible installation on AWX host (if needed)
2. awx_host_user is setup for key based authentication and sudo access on remote server

## Steps:
1. clone the repository to a local directory

        git clone https://github.com/prantikb/awx-install-rhel7.git
        
2. Change directory to repository location

        cd awx-install-rhel7
        
2. Update vars.yml as per local AWX installation requirements
3. Run the following command to start AWX installation using the playbook

        ansible-playbook -i <host_name>, site.yml -e @./vars.yml -u <awx_host_username>
