.. _calm_basics:

**********************
Calm Basics
**********************

Overview
********

.. note::

  This lab should be completed **AFTER** the :ref:`ssp_lab` lab.

  Estimated time to complete: **40 MINUTES**

In this exercise you will explore the basics of Nutanix Calm by building and deploying a Blueprint that installs and configures a single service, MySQL, on a CentOS image.

Getting Engaged with the Product Team
=====================================
- **Slack** - #calm
- **Product Manager** - Jasnoor Gill, jasnoor.gill@nutanix.com
- **Product Marketing Manager** - Chris Brown, christopher.brown@nutanix.com
- **Technical Marketing Engineer** - Brian Suhr, brian.suhr@nutanix.com
- **Field Specialists** - Mark Lavi, mark.lavi@nutanix.com; Andy Schmid, andy.schmid@nutanix.com

Calm Basics
***********

Glossary
========
- **Service**: One tier of a multiple tier application. This can be made up of 1 more VMs (or existing machines) that all have the same config and do the same thing
- **Application (App):** A whole application with multiple parts that are all working towards the same thing (for example, a Web Application might be made up of an Apache Server, a MySQL database and a HAProxy Load balancer. Alone each service doesn’t do much, but as a whole they do what they’re supposed to).
- **Macro:** A Calm construct that is evaluated and expanded before being ran on the target machine. Macros and Variables are denoted in the @@{[name]}@@ format in the scripts.
- **Subtrate:** A Calm object used to encapsulate the VM(s) within a Blueprint

Accessing Calm
==============

Open \https://<*Prism-Central-IP*>:9440/ in a browser.

Log in as **admin**.

From the navigation bar, select **Apps**.

Calm will default to the **Applications** tab, showing all instances of applications that have been launched from a Blueprint.

Tabbed Navigation
=================

Calm introduces a new sidebar to Prism Central. Note the titles and description of each tab:

.. figure:: https://s3.amazonaws.com/s3.nutanixworkshops.com/calm/lab1/image2.png

Blueprint Editor
================

The Blueprint Editor is the UI within Prism Central used to easily, graphically construct applications that consist of multiple clouds, VMs, and services. Note the key sections:

.. figure:: https://s3.amazonaws.com/s3.nutanixworkshops.com/calm/lab1/image4.png

Note the additional buttons below as they can be helpful when actively editing a Blueprint:

.. figure:: https://s3.amazonaws.com/s3.nutanixworkshops.com/calm/lab1/image5.png

In general, the Blueprint creation workflow is as follows:

- Create Object in Application Overview or select existing Object from the Workspace or Application Overview panel.
- Configure the Object in the Configuration Pane.
- Repeat for each Object.
- Connect dependencies between Objects in the Workspace.
