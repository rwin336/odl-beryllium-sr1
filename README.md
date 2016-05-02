odl-beryllium-sr1
=========
OpenDaylight Beryllium SR1 Docker container setup and install.

The playbook is desinged to install Docker on a Trusty/Xenial Ubuntu following https://docs.docker.com/engine/installation/linux/ubuntulinux/ then install/start a docker container for an OpenDayLight Beryllium controller.

The ODL controller has many features installed at boot time and ports exposed to external interface of the target Ubuntu node.  

Requirements
------------

Target Ubuntu Trusty/Xenial is setup for ansible and able to download containers from DockerHub

Process
-------
 1. Clone the following repository on a build node capable of running ansible playbooks.
 
      $ git clone https://github.com/rwin336/odl-beryllium-sr1.git

 2. Update my-hosts.ini file to include the IP Address and ssh user/password of the target Ubuntu node.
 3. Install your public ssh key on the target Ubuntu node.
 4. Run the playbook
 
      $ ansible-playbook -i my-hosts.ini ansible/odl-standup.yml
      
 5. Verify the ODL controller is up and running on the target
 
      $ docker ps -a

CONTAINER ID        IMAGE                       COMMAND             CREATED             STATUS              PORTS                                                                                            NAMES
e70e62457d4c        rwin336/odl-beryllium-sr1   "./karaf server"    2 minutes ago       Up 2 minutes        0.0.0.0:6633->6633/tcp, 0.0.0.0:8080->8080/tcp, 0.0.0.0:8101->8101/tcp, 0.0.0.0:8181->8181/tcp   odl-beryllium-sr1


License
-------

  Apache License
  Version 2.0, January 2004
  http://www.apache.org/licenses/


Author Information
------------------

R.A. Winters <rwin336@gmail.com>
