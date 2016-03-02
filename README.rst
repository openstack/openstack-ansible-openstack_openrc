OpenStack-Ansible openrc file
#############################
:tags: openstack, openrc, cloud, ansible
:category: \*nix

This Ansible role creates the configuration files used by various OpenStack
CLI tools. For more information about these tools, see the `OpenStack CLI
Reference`_.

.. _OpenStack CLI Reference: http://docs.openstack.org/cli-reference/overview.html

Required Variables
------------------

To use this role, define the following variables:

.. code-block:: yaml

    keystone_service_adminuri_insecure: false
    keystone_service_internaluri_insecure: false
    openrc_os_password: secrete
    openrc_os_domain_name: Default

Example Playbook
----------------

.. code-block:: yaml

    - name: Install openrc
      hosts: all
      user: root
      roles:
        - { role: "openstack-ansible-openstack_openrc",
            tags: [ "openstack_openrc" ]
          }
      vars:
        keystone_service_adminuri_insecure: false
        keystone_service_internaluri_insecure: false
        openrc_os_password: secrete
        openrc_os_domain_name: Default
