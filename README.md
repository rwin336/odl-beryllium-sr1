odl-beryllium-sr1
=========
OpenDaylight Beryllium SR1 Docker container setup and install.

The playbook is desinged to install Docker on a 14.04 Ubuntu following https://docs.docker.com/engine/installation/linux/ubuntulinux/ then install a docker container for an OpenDayLight Beryllium controller.

Then ODL controller has many features installed at boot time and ports exposed to external interface of the target Ubuntu node.  

Requirements
------------

Target Ubuntu 14.04 is setup for ansible and able to download containers frmo DockerHub

Process
-------
 1. Clone this repository on a build node capable of running ansible playbooks.
 2. Update my-hosts.ini file to include the IP Address and user password of the target Ubuntu node.
 3. Install you public ssh key on the target Ubuntu node.
 4. Run the playbook
 
      $ ansible-playbook -i my-hosts.ini ansible/odl-standup.yml
      
 5. Verify the ODL controller is up and running on the target
 
      $ docker ps -a



License
-------

  Apache License
  Version 2.0, January 2004
  http://www.apache.org/licenses/


Author Information
------------------

R.A. Winters <rwin336@gmail.com>
