.. title:: Introduction to Nutanix Calm

.. toctree::
  :maxdepth: 2
  :caption: Labs
  :name: _labs
  :hidden:

  enable/enable
  basics/basics
  mysql/mysql
  lamp/lamp
  marketplace_p1/marketplace_p1
  marketplace_p2/marketplace_p2
  karan/karan
  mssql/mssql

.. toctree::
  :maxdepth: 2
  :caption: Optional Labs
  :name: _optional_labs
  :hidden:

  restapi/restapi
  docker/docker
  ansible/ansible

.. toctree::
  :maxdepth: 2
  :caption: Appendix
  :name: _appendix
  :hidden:

  appendix/glossary

.. _getting_started:

---------------
Getting Started
---------------

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed velit odio, ultrices sed elementum vitae, dictum eget turpis. Etiam ultrices orci quis tempus tempus. Nulla non nibh imperdiet, suscipit risus quis, eleifend nisl. Morbi at posuere nibh, quis bibendum dui. Morbi dictum sem a ipsum bibendum condimentum. Suspendisse id ante gravida, efficitur leo a, consequat enim. Suspendisse tempor lorem vel purus scelerisque, vel facilisis lorem consequat. Pellentesque augue orci, iaculis vel mollis sit amet, scelerisque a tellus. Aliquam commodo in lectus feugiat porta.

What's New
++++++++++

- Workshop updated for the following software versions:

  - AOS 5.6
  - AFS 3.0
- Added :ref:`example_lab_3`

Access Instructions
+++++++++++++++++++

The Nutanix Hosted POC environment can be accessed a number of different ways:

Citrix XenDesktop
.................

https://citrixready.nutanix.com - *Accessible via the Citrix Receiver client or HTML5*

**Nutanix Employees** - Use your NUTANIXDC credentials

**Non-Employees** - **Username:** POCxxx-User01 (up to POCxxx-User20), **Password:** *<Provided by Instructor>*

Employee Pulse Secure VPN
..........................

https://sslvpn.nutanix.com - Use your CORP credentials

Non-Employee Pulse Secure VPN
..............................

https://lab-vpn.nutanix.com - **Username:** POCxxx-User01 (up to POCxxx-User20), **Password:** *<Provided by Instructor>*

Under **Client Application Sessions**, click **Start** to the right of **Pulse Secure** to download the client.

Install and open **Pulse Secure**.

Add a connection:

- **Type** - Policy Secure (UAC) or Connection Server
- **Name** - HPOC VPN
- **Server URL** - lab-vpn.nutanix.com
