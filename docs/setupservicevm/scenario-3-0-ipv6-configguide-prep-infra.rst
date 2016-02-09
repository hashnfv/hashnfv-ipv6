.. This work is licensed under a Creative Commons Attribution 4.0 International License.
.. http://creativecommons.org/licenses/by/4.0
.. (c) Bin Hu (AT&T) and Sridhar Gaddam (RedHat)

====================
Infrastructure Setup
====================

In order to set up the service VM as an IPv6 vRouter, we need to prepare 3 hosts,
each of which has minimum 8GB RAM and 40GB storage. One host is used as OpenStack Controller
Node. The second host is used as Open Daylight Controller Node. And the third one is used as
OpenStack Compute Node.

**Please NOTE that Although the deployment model of single controller node is assumed, in case of HA
(High Availability) deployment model where multiple controller nodes are used, there is no impact and the
setup procedure is the same.**

For exemplary purpose, we assume:

* The hostname of OpenStack Controller+Network+Compute Node is ``opnfv-os-controller``, and the host IP address
  is ``192.168.0.10``
* The hostname of OpenStack Compute Node is ``opnfv-os-compute``, and the host IP address is ``192.168.0.20``
* The hostname of Open Daylight Controller Node is ``opnfv-odl-controller``, and the host IP address is
  ``192.168.0.30``
* We use ``opnfv`` as username to login.
* We use ``devstack`` to install OpenStack Kilo. Please note that OpenStack Liberty can be used as well.

The underlay network topology of those 3 hosts are shown as follows in :numref:`s3-figure1`:

.. figure:: images/ipv6-topology-scenario-3.png
   :name: s3-figure1
   :width: 100%

   Underlay Network Topology - Scenario 3

**Please note that the IP address shown in** :numref:`s3-figure1`
**are for exemplary purpose. You need to configure your public IP
address connecting to Internet according to your actual network
infrastructure. And you need to make sure the private IP address are
not conflicting with other subnets**.
