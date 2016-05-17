# Hadoop Bootstrap

There are several steps that each Hadoop environment requires upon setup. In
order to ease the setup this playbook was created.

Prerequisites:
* Ansible is set up
* Connection to hosts established
* Fully qualified domain names are entered in the correct section in the hosts
  file


## Usage

Execute _./cloudera-single-node-centos7-ec2.yml_ in order to provision an EC2
node, prepare the nodes for hadoop and download cloudera manager.

User _--ask-vault-pass_ in case you use an encrypted variables file.
