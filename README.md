NAME
====

amount - auto mount

SYNOPSIS
========

    amount sdb1         (mount /dev/sdb1)
    amount /dev/sdb1    (the same)
    amount -h           (help)

DESCRIPTION
===========

amount allows to easily mount and unmount devices.

When user mounts a device, a new subshell is started. The device is unmounted
when the subshell is closed. User can check which device is bound to the current
subshell using AMOUNT_DEVICE environmental variable.

EXAMPLE
-------

    $ amount sdb1
    * /dev/sdb1 mounted
    $ echo $AMOUNT_DEVICE
    /dev/sdb1
    $ pwd
    /media/sdb1
    $ exit
    * Unmounting /dev/sdb1...
    * /dev/sdb1 unmounted
    $ echo $AMOUNT_DEVICE

    $

INSTALLATION
============

Just copy _amount_ file to your PATH (for example /usr/local/bin).

DEPENDENCIES
------------

pmount, bash

AUTHOR
======

Wojciech 'vifon' Siewierski < wojciech dot siewierski at gmail dot com >

COPYRIGHT
=========

Copyright (C) 2012  Wojciech Siewierski

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
