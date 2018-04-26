.. title:: Introduction to Nutanix Calm

.. toctree::
  :maxdepth: 2
  :caption: Labs
  :name: _labs
  :hidden:

  enable/enable
  mysql/mysql
  lamp/lamp
  marketplace_p1/marketplace_p1
  marketplace_p2/marketplace_p2
..  karan/karan
..  mssql/mssql

.. toctree::
  :maxdepth: 2
  :caption: Optional Labs
  :name: _optional_labs
  :hidden:

..  restapi/restapi
..  docker/docker
..  ansible/ansible

.. toctree::
  :maxdepth: 1
  :caption: Appendix
  :name: _appendix
  :hidden:

  appendix/basics

.. _getting_started:

---------------
Getting Started
---------------

.. raw:: html

  <strong><font color="red">Please do not start any labs before reviewing the information on this page.</font></strong><br><br>

Nutanix Workshops provides hands-on guides for understanding and implementing a variety of solutions on top of the leading Enterprise Cloud Platform.

In this introductory Workshop you will explore Nutanix's new application-centric automation platform built directly into Prism Central. You will build multi-tier application Blueprints from scratch and deploy additional Blueprints from the Nutanix Marketplace. After completing the Workshop you should have an understanding of Calm's core functionalities and the value Calm provides within an IT organization.

Prior to beginning the labs, be sure to review :ref:`calm_basics` to familiarize yourself with the UI and common terminology used in Nutanix Calm.

What's New
++++++++++

**Coming Soon!**

- Using Calm with Windows workloads
- Building custom Blueprint actions
- Using the Calm REST API
- Deploying Calm Blueprints to the public cloud

**April 27th, 2018 Updates**

- Workshop updated for AOS 5.6 and AHV 20170830.115

Environment Details
+++++++++++++++++++

Nutanix Workshops are intended to be run in the Nutanix Hosted POC environment. Your cluster will be provisioned with all necessary images, networks, and VMs required to complete the exercises.

Networking
..........

Hosted POC clusters follow a standard naming convention, where the numerical suffix corresponds to the subnet for that cluster:

- **Cluster Name** - POC\ *XYZ*
- **Subnet** - 10.21.\ *XYZ*\ .0
- **Cluster IP** - 10.21.\ *XYZ*\ .37

For example:

- **Cluster Name** - POC055
- **Subnet** - 10.21.55.0
- **Cluster IP** - 10.21.55.37

Throughout the Workshop there are multiple instances where you will need to substitue *XYZ* with the correct octet for your subnet, for example:

.. list-table::
   :widths: 25 75
   :header-rows: 1

   * - IP Address
     - Description
   * - 10.21.\ *XYZ*\ .37
     - Nutanix Cluster Virtual IP
   * - 10.21.\ *XYZ*\ .39
     - **PC** VM IP, Prism Central
   * - 10.21.\ *XYZ*\ .40
     - **DC** VM IP, NTNXLAB.local Domain Controller

Each cluster is configured with 2 VLANs which can be used for VMs:

.. list-table::
  :widths: 25 25 10 40
  :header-rows: 1

  * - Network Name
    - Address
    - VLAN
    - DHCP Scope
  * - Primary
    - 10.21.\ *XYZ*\ .1/25
    - 0
    - 10.21.\ *XYZ*\ .50-10.21.\ *XYZ*\ .124
  * - Secondary
    - 10.21.\ *XYZ*\ .129/25
    - *XYZ1*
    - 10.21.\ *XYZ*\ .132-10.21.\ *XYZ*\ .253

Credentials
...........

.. note::

  The *<Cluster Password>* is unique to each cluster and will be provided by the leader of the Workshop.

.. list-table::
   :widths: 25 35 40
   :header-rows: 1

   * - Credential
     - Username
     - Password
   * - Prism Element
     - admin
     - *<Cluster Password>*
   * - Prism Central
     - admin
     - *<Cluster Password>*
   * - Controller VM
     - nutanix
     - *<Cluster Password>*
   * - Prism Central VM
     - nutanix
     - *<Cluster Password>*

Each cluster has a dedicated domain controller VM, **DC**, responsible for providing AD services for the **NTNXLAB.local** domain. The domain is populated with the following Users and Groups:

.. list-table::
   :widths: 25 35 40
   :header-rows: 1

   * - Group
     - Username(s)
     - Password
   * - Administrators
     - Administrator
     - nutanix/4u
   * - SSP Admins
     - adminuser01-adminuser25
     - nutanix/4u
   * - SSP Developers
     - devuser01-devuser25
     - nutanix/4u
   * - SSP Power Users
     - poweruser01-poweruser25
     - nutanix/4u
   * - SSP Basic Users
     - basicuser01-basicuser25
     - nutanix/4u

Access Instructions
+++++++++++++++++++

The Nutanix Hosted POC environment can be accessed a number of different ways:

Citrix XenDesktop
.................

https://citrixready.nutanix.com - *Accessible via the Citrix Receiver client or HTML5*

**Nutanix Employees** - Use your NUTANIXDC credentials

**Non-Employees** - **Username:** POC\ *XYZ*\ -User01 (up to POC\ *XYZ*\ -User20), **Password:** *<Cluster Password>*

Employee Pulse Secure VPN
..........................

https://sslvpn.nutanix.com - Use your CORP credentials

Non-Employee Pulse Secure VPN
..............................

https://lab-vpn.nutanix.com - **Username:** POC\ *XYZ*\ -User01 (up to POC\ *XYZ*\ -User20), **Password:** *<Cluster Password>*

Under **Client Application Sessions**, click **Start** to the right of **Pulse Secure** to download the client.

Install and open **Pulse Secure**.

Add a connection:

- **Type** - Policy Secure (UAC) or Connection Server
- **Name** - HPOC VPN
- **Server URL** - lab-vpn.nutanix.com
