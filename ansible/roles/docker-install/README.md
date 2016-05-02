docker-install
=========

The playbook is desinged to install Docker on a Ubuntu Trusty/Xenial following https://docs.docker.com/engine/installation/linux/ubuntulinux/

Requirements
------------

Target Ubuntu node is setup for ansible.


Role Variables
--------------

None

Dependencies
------------

None


Example Playbook
----------------

---
  - hosts: odl-controller
    become: yes
    become_method: sudo

    roles:
      - docker-install
      - odl-install

License
-------

  Apache License
  Version 2.0, January 2004
  http://www.apache.org/licenses/


Author Information
------------------

R.A. Winters <rwin336@gmail.com>