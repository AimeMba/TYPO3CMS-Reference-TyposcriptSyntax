.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. _constants:

Constants
^^^^^^^^^


.. _what-are-constants:

What are constants?
"""""""""""""""""""

Constants are values defined in the "Constants"-field of a template.
They follow the syntax of ordinary TypoScript and are case sensitive!
They allow to manage a value, which should later be used at *several
places*, to be maintained centrally at only *one single place*.

**Note, reserved name:** The object or property "file" is always
interpreted as data type "resource". That means it refers to a file,
which you have to upload in the resource section of your template
record.

**Note: The top-level "object" TSConstantEditor** cannot be used. It's
reserved for configuration of the Constant Editor module.


Example:
~~~~~~~~

Here "bgCol" is set to "red" and "file.toplogo" is set to "logo.gif".
which is found in the resource-field of the template. ::

   bgCol = red
   topimg.width = 200
   topimg.file.pic2 = fileadmin/logo2.gif
   file.toplogo = logo.gif

This could also be defined in other ways, e.g. like this::

   bgCol = red
   file {
     toplogo = logo.gif
   }
   topimg {
     width = 200
     file.pic2 = fileadmin/logo2.gif
   }

(The objects in bold are the reserved word "file" and the properties
are always of data type "resource".)

.. figure:: ../../Images/TSTemplatesConstants.png
   :alt: Overview of the defined constants.

