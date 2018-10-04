.. _download-verify-decompress-windows:

Download, verify, and decompress a |CL-ATTR| image on Windows\*
###############################################################

This guide describes the types of |CL-ATTR| images available, where to download
them, how to verify the integrity of an image, and how to decompress it.

Instructions for other operating systems are available:

* :ref:`download-verify-decompress-linux`
* :ref:`download-verify-decompress-mac`

Image types
***********

.. include:: ../../reference/image-types.rst
   :start-after: image-types-content:

.. _verify-windows:

Verify the integrity of the |CL| image
**************************************

Before you use a downloaded |CL| image, verify its integrity. This action
eliminates the small chance of a corrupted image due to download issues. To
support verification, each released |CL| image has a corresponding SHA512
checksum file designated with the suffix `-SHA512SUMS`.

#.  Download the corresponding SHA512 checksum file of your |CL| image.
#.  Start Command Prompt.
#.  Go to the directory with the downloaded image and checksum files.
#.  Get the SHA512 checksum of the image with the command:

    .. code-block:: bash

        CertUtil -hashfile ./clear-[version number]-[image type].[compression type] sha512

#.  Manually compare the output with the original checksum value shown in
    the downloaded checksum file and make sure they match.

Decompress the |CL| image
********************************

Released |CL| images are compressed with either GNU zip (*.gz*) or XZ
(*.xz*). The compression type depends on the target platform or
environment. To decompress the image, follow these steps:

#. Download and install `7-Zip`_.
#. Go to the directory with the downloaded image and right-click it.
#. From the pop-up menu, select :guilabel:`7-Zip` and select
   :guilabel:`Extract Here` as shown in Figure 1.

   .. figure:: figures/download-verify-decompress-windows-fig-1.png
      :scale: 80 %
      :alt: 7-Zip extract file

      Figure 1: Windows 7-Zip extract file.

.. _7-Zip: http://www.7-zip.org/
