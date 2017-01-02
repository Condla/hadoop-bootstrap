Role Name
=========

* This role should be used to install and configure your operating system before
you plan to install Apache Hadoop and its Ecosystem components.

* It also installs all packages and libraries required to secure the cluster
using the Kerberos protocol.

* The first thing it does per default is to install the epel repository, which is
  needed to install python-pip. Pip is required to install several client tools for Hadoop.
  If you do not wish to install epel, set the variable ```install_epel``` to
  ```no``` in your playbook.



Requirements
------------

* A CentOS-7.x or RHEL 7.x
* all kernel updates already done: this is important since there might be changes
  in the kernel configuration. If you update the kernel *and* change its configuration
  the instance might not boot

Role Variables
--------------

### Security Related Variables:

krb_realm:


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
