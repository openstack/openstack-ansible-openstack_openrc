=============================
OpenStack-Ansible openrc file
=============================

This Ansible role creates the configuration files used by various
OpenStack CLI tools. For more information about these tools, see the
`OpenStack CLI Reference`_.

.. _OpenStack CLI Reference: http://docs.openstack.org/cli-reference/overview.html

Default variables
~~~~~~~~~~~~~~~~~

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.

Required variables
~~~~~~~~~~~~~~~~~~

To use this role, define the following variables:

.. code-block:: yaml

    keystone_service_adminuri_insecure: false
    keystone_service_internaluri_insecure: false
    openrc_os_password: secrete
    openrc_os_domain_name: Default

Tags
~~~~

This role supports two tags: ``openrc-install`` and ``openrc-config``.
The ``openrc-install`` tag can be used to install and upgrade. The
``openrc-config`` tag can be used to manage configuration.


Example playbook
~~~~~~~~~~~~~~~~

.. literalinclude:: ../../examples/playbook.yml
   :language: yaml
