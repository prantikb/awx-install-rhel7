# awx-install-rhel7
Install AWX on RHEL 7

Pre-Requisites:
1. Enable Ansible Repository for ansible installation on AWX host
        sudo subscription-manager repos --enable rhel-7-server-ansible-2.9-rpms

Steps:
1. clone the repository to a local directory
        git clone https://github.com/prantikb/awx-install-rhel7.git
2. Change directory to repository location
        cd awx-install-rhel7
2. Update vars.yml as per local AWX installation requirements
3. Run the following command to start AWX installation using the playbook

        ansible-playbook -i <host_name>, site.yml -e @./vars.yml
