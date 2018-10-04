.. _bootable-usb-mac:

Create a bootable USB drive on macOS
####################################

Follow these instructions to create a bootable |CL-ATTR| USB drive.
Use an **8GB** or larger USB drive. Download either a live image, 
``clear-<version>-live.img.xz`` or an installer image, 
``clear-<version>-installer.img.xz``, from our `image`_ download page. 

Instructions are also available for other operating systems:

* :ref:`bootable-usb-linux`
* :ref:`bootable-usb-windows`

.. include:: ../../reference/image-types.rst
   :start-after: incl-image-filename: 
   :end-before: incl-image-filename-end:

.. include:: ../../guides/maintenance/download-verify-decompress-mac.rst
   :start-after: verify-mac:


Burn the |CL| image onto a USB drive
************************************

.. caution::

   |CAUTION-BACKUP-USB|

#. Launch the Terminal app.
#. Go to the directory with the decompressed image.
#. Plug in a USB drive and get its identifier by entering the command
   :command:`diskutil list`.  See Figure 1.

   .. code-block:: console

      diskutil list

   .. figure:: figures/bootable-usb-mac-1.png
      :scale: 100 %
      :alt: Get USB drive identifier

      Figure 1: macOS - Get USB drive identifier

#. Unmount the USB drive identified in the previous step.  The command-line
   example below umounts `/dev/disk2`:

   .. code-block:: console

      diskutil umountDisk /dev/disk2

#. Burn the image onto the drive using the :command:`dd` command.  The 
   command-line example below burns an uncompressed image onto `/dev/disk2`:

   .. code-block:: console

      sudo dd if=./clear-[version number]-[image type] of=/dev/rdisk2 bs=4m


   Adding an ‘r’ in front of the disk identifier should help speed up the 
   imaging process.
   
   You can press :kbd:`<CTL>-T` to check imaging progress.

#. Eject the USB drive.

   .. code-block:: console

      diskutil eject /dev/disk2

Next steps
**********

With a bootable |CL| USB drive, you can:

* :ref:`bare-metal-install`
* :ref:`boot-live-image`
* :ref:`multi-boot`

.. _image: https://download.clearlinux.org/image
