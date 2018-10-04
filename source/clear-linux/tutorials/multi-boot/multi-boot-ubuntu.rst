.. _multi-boot-ubuntu:

Install Ubuntu\* 16.04 LTS Desktop
##################################

This guide describes Ubuntu-specific details of the :ref:`multi-boot`
tutorial.

#. Start the Ubuntu installer and follow the prompts.

#. At the :guilabel:`Installation type` screen, choose
   :guilabel:`Something else`. See Figure 1.

   .. figure:: figures/multi-boot-ubuntu-1.png

      Figure 1: Ubuntu: Installation type.

#. Create a new root partition.

   #. Under the :guilabel:`Device` column, select :guilabel:`free space`. See
      Figure 2.

      .. figure:: figures/multi-boot-ubuntu-2.png

         Figure 2: Ubuntu: Add partition.

   #. Click the :guilabel:`+` button on the lower left corner.

   #. Enter the new partition size. For this example, we used *40000 MB*, as
      shown in Figure 3.

      .. figure:: figures/multi-boot-ubuntu-3.png

         Figure 3: Ubuntu: Configure new root partition.

   #. Set :guilabel:`Use as` to :guilabel:`Ext4 journaling file system`.

   #. Set the :guilabel:`Mount point` to `/`.

   #. Click :guilabel:`OK`.

   #. Under the :guilabel:`Format?` column, select the new partition to be
      formatted, in this example :file:`/dev/sda8`.

#. Share the swap partition that was created by |CL|.

   #. Under the :guilabel:`Device` column, select :file:`/dev/sda2`.

   #. Click :guilabel:`Change`.

   #. Confirm :guilabel:`Use as` is set to :guilabel:`swap area`. See Figure 4.

      .. figure:: figures/multi-boot-ubuntu-4.png

         Figure 4: Ubuntu: Set swap partition.

#. Follow the remaining prompts to complete the Ubuntu installation.

#. At this point, you cannot boot |CL| because `Grub`
   is the default boot loader. Follow these steps to make the |CL|
   Systemd-Boot the default boot loader and add Ubuntu as a boot option:

   #. Boot into Ubuntu.

   #. Log in.

   #. Locate the Ubuntu :file:`grub.cfg` file in the :file:`/boot/grub/`
      directory and look for the :guilabel:`menuentry` section. In Figure 5, the
      highlighted lines identify the kernel, the :file:`initrd` files, the
      root partition UUID, and the additional parameters used. Use this
      information to create a new Systemd-Boot entry for Ubuntu.

      .. figure:: figures/multi-boot-ubuntu-5.png

         Figure 5: Ubuntu: grub.cfg file.

   #. Copy the kernel and the :file:`initrd` file to the EFI partition.

      .. code-block:: bash

         sudo cp /boot/vmlinuz-4.8.0-36-generic.efi.signed /boot/efi

         sudo cp /boot/initrd.img-4.8.0-36-generic /boot/efi

   #. Create a boot entry for Ubuntu. At a minimum, the file must contain
      these settings:

      +---------+------------------------------------+
      | Setting | Description                        |
      +=========+====================================+
      | title   | Text to show in the boot menu      |
      +---------+------------------------------------+
      | linux   | Linux kernel image                 |
      +---------+------------------------------------+
      | initrd  | initramfs image                    |
      +---------+------------------------------------+
      | options | Options to pass to the EFI program |
      |         | or kernel boot parameters          |
      +---------+------------------------------------+

      See the `systemd boot loader documentation`_ for additional
      details.

      The *options* parameters must specify the root partition UUID and
      any additional parameters that Ubuntu requires.

      .. note:: The root partition UUID used below is unique to this example.

      .. code-block:: bash

         sudoedit /boot/efi/loader/entries/ubuntu.conf

      Add the following lines to the :file:`ubuntu.conf` file:

      .. code-block:: console

         title Ubuntu 16.04 LTS Desktop

         linux /vmlinuz-4.8.0-36-generic.efi.signed

         initrd /initrd.img-4.8.0-36-generic

         options root=UUID=17f0aa66-3467-4f99-b92c-8b2cea1045aa ro

#. Re-install Systemd-Boot to make it the default boot loader.

   .. code-block:: bash

      sudo bootctl install --path /boot/efi

   .. note::
      If an older version of Ubuntu does not have the `bootctl` command,
      skip this step and see :ref:`multi-boot-restore-bl` to restore
      Systemd-Boot.

#. Reboot.

If you want to install other :abbr:`OSes (operating systems)`, refer to
:ref:`multi-boot` for details.

.. _systemd boot loader documentation:
   https://wiki.archlinux.org/index.php/Systemd-boot
