.. include:: /Includes.rst.txt
.. index:: Backend users; Privileges
.. _privileges:

==================
Backend privileges
==================

The following chapters cover modules that will only be available for backend
users with specific access privileges.

In addition to configuring access
rights for backend users or groups as described in :ref:`permissions`, there
are "superuser" rights which can be activated for each user.

If a backend user has been created for editing in the backend, he or she should
usually not get access to admin or system modules.

You should only give a backend user
as much access as is needed. This makes the job easier by automatically deactivating
modules and GUI elements the user does not have access to. It also makes it
impossible for a user to damage the system by accidentally doing things he or she
should not have been able to do in the first place.

Before TYPO3 version 9 there was only admin and non admin. Now we have the
additional access privilege "system maintainer".



.. index::
   Backend users; Admin
   pair: Privileges; Admin
.. _admin-user:

Admin
=====

* admin user privilege can be added by clicking the "admin" checkbox when
  creating or changing a backend user
* admins have access to the **SYSTEM** module (including Access, Backend User,
  Log etc. modules)

.. image:: ../../Images/system.png
   :class: with-shadow

.. image:: ../../Images/system_open.png
   :class: with-shadow



.. index::
   Backend users; System maintainers
   pair: Privileges; System maintainers
.. _user-management-system-maintainers:
.. _system-maintainer:

System maintainers
==================

The first backend admin created during installation will automatically be a system
maintainer as well. To give other users system privileges, you
can add them in the :guilabel:`ADMIN TOOLS > Settings > Manage System Maintainers`
configuration.
Alternatively the website can be set into "Development" mode in the Install
Tool. This will give all admin users system maintainer access.

.. image:: ../../Images/admin-tools.png
   :class: with-shadow

.. image:: ../../Images/admin-tools-open.png
   :class: with-shadow

System Maintainers are the only users who are able to see and access the Install Tool
and the Extension Manager. These users are persisted within the
:file:`LocalConfiguration.php` as :php:`$GLOBALS['TYPO3_CONF_VARS']['SYS']['systemMaintainers']`.


