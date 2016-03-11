.. _d:version:

15. Version (O)
---------------
The version number of the resource (occurrences: 0-1).

**Allowed values, examples, other constraints**

Suggested practice: track major_version.minor_version.

Register a new identifier for a major version change. Individual stewards need to determine which are major vs. minor versions (based on the work of the Earth Science Information Partners (ESIP). For more guidance, see `here <http://wiki.esipfed.org/index.php/Interagency_Data_Stewardship/Citations/provider_guidelines#Note_on_Versioning_and_Locators>`_.

May be used in conjunction with properties :ref:`d:alternateidentifier` and :ref:`d:relatedidentifier` to indicate various information updates.

May be used in conjunction with property :ref:`d:description` to indicate the nature and file/record range of version.

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <version>1.0</version>
