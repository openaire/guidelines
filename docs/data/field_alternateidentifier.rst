.. _d:alternateidentifier:

11. AlternateIdentifier (O)
---------------------------

An identifier or identifiers other than the primary Identifier applied to the resource being registered. This may be any alphanumeric string which is unique within its domain of issue. May be used for local identifiers. AlternateIdentifier should be used for another identifier of the same instance (same location, same file) (occurrences: 0-n).

**Allowed values, examples, other constraints**

.. _d:alternateidentifiertype:

11.1 alternateIdentifierType (O)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The type of the AlternateIdentifier (occurrences: 1).

**Allowed values, examples, other constraints**

Free text.

If AlternateIdentifier is used, alternateIdentifierType is mandatory. For the above example, the alternateIdentifierType would be ``A local accession number``.

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <alternateIdentifiers>
    <alternateIdentifier alternateIdentifierType="ISBN">
        937-0-1234-56789-X
    </alternateIdentifier>
   </alternateIdentifiers>
