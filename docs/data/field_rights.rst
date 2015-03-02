.. include:: ../common/replacements.rst

.. _d:rights:

16. Rights (MA)
---------------
Any rights information for this resource (occurrences: 0-n).

**Allowed values, examples, other constraints**

Free text.

Provide a rights management statement for the resource or reference a service providing such information. Include embargo information if applicable.

Use the complete title of a license and include version information if applicable.

Example: Creative Commons Attribution 3.0 Germany License

.. note::

   *Mandatory when applicable* property in OpenAIRE instead of optional in DataCite.

   OpenAIRE uses this property to explicit declare the access right of the resource via :ref:`d:rightsuri`. This does not exclude also using :ref:`d:rights` property for additional rights statements as defined by DataCite Metadata Schema |datacitever|. In particular OpenAIRE also recommends including license information if available.

   Please refer to the section :ref:`accessrights` for a full example of how to declare access right and license information.

.. _d:rightsuri:

16.1 rightsURI (MA)
~~~~~~~~~~~~~~~~~~~
The URI of the license (occurrences: 0-1).

**Allowed values, examples, other constraints**

Example:

http://creativecommons.org/licenses/by/3.0/de/deed.en

.. note::

   *Mandatory when applicable* property in OpenAIRE instead of optional in DataCite.

   Use terms from the `info:eu-repo-Access-Terms vocabulary <http://purl.org/eu-repo/semantics/#info-eu-repo-AccessRights>`_. The values are:

   * ``info:eu-repo/semantics/closedAccess``
   * ``info:eu-repo/semantics/embargoedAccess``
   * ``info:eu-repo/semantics/restrictedAccess``
   * ``info:eu-repo/semantics/openAccess``

   This property may also be used to explicitly declare the license for the resource.

   Please refer to the section :ref:`accessrights` for a full example of how to declare access right and license information.


Example
~~~~~~~

.. include:: examples/accessright.rst
