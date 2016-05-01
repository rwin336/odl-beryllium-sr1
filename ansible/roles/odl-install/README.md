odl-install
=========

Install rwin336/odl-beryllium-sr1 docker container on the target node.
The ODL Controller is started with at least the following features installed:

    odl-netconf-api
    odl-netconf-mapping-api
    odl-netconf-util
    odl-netconf-impl
    odl-config-netconf-connector
    odl-netconf-netty-util
    odl-netconf-monitoring
    odl-netconf-notifications-api
    odl-netconf-notifications-impl
    odl-yangtools-models
    odl-yangtools-data-binding
    odl-yangtools-binding
    odl-yangtools-binding-generator
    http
    war
    odl-config-persister
    odl-config-startup
    pax-jetty
    pax-http
    pax-http-whiteboard
    pax-war
    odl-akka-scala
    odl-akka-system
    odl-akka-clustering
    odl-akka-leveldb
    odl-akka-persistence
    odl-mdsal-common
    odl-mdsal-broker-local
    odl-mdsal-clustering-commons
    odl-mdsal-distributed-datastore
    odl-mdsal-remoterpc-connector
    odl-mdsal-broker
    odl-config-netty
    odl-aaa-authn
    odl-restconf
    odl-restconf-noauth

Requirements
------------

The node needs to be ablt to access DockerHub where the rwin336/odl-beryllium-sr1 container resides

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