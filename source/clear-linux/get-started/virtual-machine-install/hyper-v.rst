.. _hyper-v:

Use Hyper-V\*
#############

This section explains how to run |CL-ATTR| inside a
`Windows Server Virtualization`_\* or **Hyper-V** environment.

Please ensure you have enabled `Intel® Virtualization Technology
<http://www.intel.com/content/www/us/en/virtualization/virtualization-technology/intel-virtualization-technology.html>`_
(Intel® VT) and `Intel® Virtualization Technology for Directed I/O
<https://software.intel.com/en-us/articles/intel-virtualization-technology-for-directed-io-vt-d-enhancing-intel-platforms-for-efficient-virtualization-of-io-devices>`_
(Intel® VT-d) in your BIOS/UEFI firmware configuration.

Enable Hyper-V
**************

Please refer to the `Microsoft documentation`_ to enable and configure
*Hyper-V* on your machine.

Create a virtual network
************************

Once *Hyper-V* has been enabled on your Windows system you will need to 
create a virtual network in the **Hyper-V Manager**.  Refer to the
`Create a Virtual Network documentation`_ to create and configure
a virtual network.

Create a virtual machine
************************

#. Download and decompress the latest hyperv disk image
   :file:`clear-XXXXX-hyperv.img.gz`, where XXXXX is the latest 
   available version of |CL| from our `downloads`_ section.

#. Create a virtual machine using the **Hyper-V Manager**:

   a. Choose **Generation 2** when prompted to *specify VM generation*.
   b. Choose **Use an existing virtual hard disk** and browse to find the
      :file:`clear-XXXX-hyperv.vhdx` file.
   c. When finished, open VM settings, select Firmware Section and in Secure
      Boot config, **uncheck** Enable Secure Boot.

   .. note:: Currently, |CL| does not boot with `secure boot`
      enabled.

#. Connect to your new VM and start it. You should see a prompt:

   .. code-block:: console

      > User: root

#. Set a root user password.

Your virtual machine running |CL| is ready!

.. _Windows Server Virtualization: https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/about/
.. _Microsoft documentation: https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v
.. _Create A Virtual Network documentation: https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/connect-to-network
.. _downloads: https://download.clearlinux.org/image/
