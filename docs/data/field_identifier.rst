.. _d:identifier:

1. Identifier (M)
-----------------
The Identifier is a unique string that identifies a resource (occurrences: 1).

**Allowed values, examples, other constraints**

Format should be “10.1234/foo”

.. _d:identifiertype:

1.1 identifierType (M)
~~~~~~~~~~~~~~~~~~~~~~
The type of the Identifier (occurrences: 1).

**Allowed values, examples, other constraints**

*Controlled list values (DataCite)*

* DOI

*Controlled list values (OpenAIRE)*

* ARK
* DOI
* Handle
* PURL
* URN
* URL

.. note::
   Unlike DataCite, OpenAIRE allows for DOIs and other types of identifiers.

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <identifier identifierType="DOI">
    10.1594/WDCC/CCSRNIES_SRES_B2
   </identifier>

