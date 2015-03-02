.. _dc:date_embargo:

Embargo End Date (MA)
^^^^^^^^^^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:date``

Usage
~~~~~
*Mandatory when applicable*

Usage Instruction
~~~~~~~~~~~~~~~~~
When :ref:`dc:rights_accesslevel` is set to

* ``info:eu-repo/semantics/embargoedAccess``

the end date of the embargo period must be provided. The corresponding term is defined by

* ``info:eu-repo/date/embargoEnd/<YYYY-MM-DD>``

Encoding of this date should be in the form ``YYYY-MM-DD`` conforming to ISO 8601.

Since
~~~~~
OpenAIRE Guidelines v1

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <dc:date>info:eu-repo/date/embargoEnd/2015-12-31</dc:date>
