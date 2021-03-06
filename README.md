# Ansible Automation Platform Lab Builder

## Purpose
* Creates VMs in your hypervisor platform of choice<sup>[1](#1.-supported-hypervisors)</sup>
    * 1 Ansible Tower
    * 1 Automation Hub
    * 1 Ansible Tower Database
    * 1 Podman
* Deploys Ansible Tower and Automation Hub
* Deploys Red Hat SSO in a container
* Configures Red Hat SSO with sample users and groups
* Configures Ansible Tower to be prepopulated with sample credentials, projects, inventories, and job templates
* Configures Ansible Tower to use Red Hat SSO for authentication

### Authentication
Keycloak is deployed with user federation linked to an openldap container that is prepopulated with users and groups as defined in the `ldap_config` section of the inventory file.
phpldapadmin is also deployed for easier management and viewing of the ldap user structure.

#### 1. Supported Hypervisors
* VMWare vCenter
    * Tested with 7.0
* Red Hat Virtualization
* OVirt