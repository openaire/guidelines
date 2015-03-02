.. _dc:rights_licensecondition:

License Condition (R)
^^^^^^^^^^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:rights``

Usage
~~~~~

*Recommended*

DCMI Definition
~~~~~~~~~~~~~~~

Information about rights held in and over the resource.

Usage Instruction
~~~~~~~~~~~~~~~~~

Typically, a rights element will contain a rights management statement for the access or use of the object, or reference a service providing such information. Rights information often encompasses Intellectual Property Rights (IPR), Copyright, and various Property Rights. It is preferred to refer to a rights service where the reuse rights are made clear to the end-user by using a URL. For example the Creative Commons organisation has created URIs for their different licences in the different jurisdictions. This can be applied to create machine readable usage licenses.

Since
~~~~~

OpenAIRE Guidelines v3

Example
~~~~~~~

.. FIXME

Generic usage examples:

.. code-block:: xml
   :linenos:

   <dc:rights>(c) University of Bath, 2003</dc:rights>
   <dc:rights>(c) Andrew Smith, 2003</dc:rights>

Using Creative Commons right services, makes the usage rights much more clear to the end user. More information see "Use of Intellectual Property Rights". In this case Andrew Smith referring to http://creativecommons.org/licenses/by-sa/2.0/uk/

.. code-block:: xml
   :linenos:

   <!-- example 1 -->
   <dc:rights>
     http://creativecommons.org/licenses/by-sa/2.0/uk/
   </dc:rights>

The URL provides the location where the license can be read. With creative common licenses the type of license can be recognized in the URL name itself. A pro for having the license point to an URL in this way, is that this is machine readable.

.. code-block:: xml
   :linenos:

   <!-- example 2 -->
   <dc:rights>cc-by-sa, Andrew Smith</dc:rights>

The string cc-by-sa provides the licence type in a rough sense. The name is the person or party where the rights apply to.

.. code-block:: xml
   :linenos:

   <!-- example 3 -->
   <dc:rights>cc-by-sa, info:eu-repo/dai/nl/344568</dc:rights>

or:

.. code-block:: xml
   :linenos:

   <dc:rights>cc-by-nc-sa, urn:isni:234562-2</dc:rights>

Also a Digital Author Identifier (DAI) or International Standard Name Identifier (ISNI) can be used to globally uniquely identify persons and organisations and relate these names with the appropriate rights.
