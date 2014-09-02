mist backends
*************

Mist gives you the opportunity to handle multiple machines on multiple providers from one interface, the mist.io service.
In order to do so, the very first thing to do when using mist.io is to ensure that you have added your backends.
After doing that you'll be able to provision, monitor and in general handle all your machines on all
those providers.

Supported Providers
===================
Before you add a new backend, you'll find it useful to see a list of all the providers that mist.io supports::

    mist ls providers

From here on you'll need your desired provider's id in order to use it when adding a new backend.

Backend Actions
===============
To add a new backend you'll need at least the provider's id, a name for the backend, an apikey/username and
apisecret/password. For example, in order to add a Rackspace backend::

    mist add backend --name RackBackend --provider rackspace:ord --key rackspace_username --secret rackspace_secret_key

You can now see a list of all your added backends::

    mist ls backends

You can also display information about a specific backend, either by providing the backend's name or ID. The following
commands are equivalent::

    mist show backend --name EC2
    mist display backend --id D1g9abwqGUmQuZKGGBMfCgw8AUQ

You have the option to rename a backend::

    mist rename backend --name EC2 --new_name RenamedBackend

Finally you can delete a backend. The following two command are equivalent::

    mist delete backend --name DigitalOcean
    mist rm backend --id D1g9abwqGUmQuZKGGBMfCgw8AUQ

You can see a full use case `here`_

.. _here: http://asciinema.org/a/11875