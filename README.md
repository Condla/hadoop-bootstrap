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

### Default variables:

* hadoop_db: Defines which db will be used for the Hadoop installation that will
be done.

### Security Related Variables:

* krb_realm: Define the realm you want to be using for your KDC
* kdc_hostname: configure where your KDC is running
* kdc_admin_hostname: configure where kdc admin instance is running
* krb_domain: define krb_domain


Dependencies
------------

condla/hdp-instances

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
- name: bootstrap hosts for the hadoop installation
  hosts: hdp
  gather_facts: yes
  become: yes
  roles:
    - hadoop-bootstrap
```

License
-------

BSD

Author Information
------------------

Stefan Kupstaitis-Dunkler (stefan.dun@gmail.com)
