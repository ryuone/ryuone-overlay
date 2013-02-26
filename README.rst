ryuone-overlay
==============

ryuone's portage overlay.

* dev-db/riak

installation
------------

1. install `app-portage/layman`

.. code-block:: shell

    # flaggie app-portage/layman +git
    # emerge -av layman


2. Add the overlay.

.. code-block:: shell

    # curl https://raw.github.com/ryuone/ryuone-overlay/master/profiles/layman.xml > /etc/layman/overlays/ryuone-overlay.xml
    # layman -f -a ryuone

3. Edit `/etc/portage/make.conf` for require layman `make.conf`.

.. code-block:: shell

   # echo 'source /var/lib/layman/make.conf' >> /etc/portage/make.conf
