.. _d:creator:

2. Creator (M)
--------------
The main researchers involved in producing the data, or the authors of the publication, in priority order (occurrences: 1-n).

**Allowed values, examples, other constraints**

May be a corporate/institutional or personal name. Note: DataCite infrastructure supports up to between 8000‐10000 names. For name lists above that size, consider attribution via linking to the related metadata.

.. _d:creatorname:

2.1 creatorName (M)
~~~~~~~~~~~~~~~~~~~
The name of the creator (occurrences: 1).

**Allowed values, examples, other constraints**

Examples: Smith, John; Miller, Elizabeth

The personal name format should be: family, given. Non‐roman names may be transliterated according to the `ALA‐LC <http://www.loc.gov/catdir/cpso/roman.html>`_ schemes.

.. _d:creator_nameidentifier:

2.2 nameIdentifier (R)
~~~~~~~~~~~~~~~~~~~~~~
Uniquely identifies an individual or legal entity, according to various schemes (occurrences: 0-1).

**Allowed values, examples, other constraints**

The format is dependent upon scheme.

.. note::
   OpenAIRE recommends including a nameIdentifier such as an ORCID or a ISNI if available.

.. _d:creator_nameidentifierscheme:

2.2.1 nameIdentifierScheme (R)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
The name of the name identifier scheme (occurrences: 1).

**Allowed values, examples, other constraints**

If nameIdentifier is used, nameIdentifierScheme is mandatory.
Examples: `ORCID <http://orcid.org>`_, `ISNI <http://www.isni.org/>`_,

.. _d:creator_schemeuri:

2.2.2 schemeURI (R)
^^^^^^^^^^^^^^^^^^^
The URI of the name identifier scheme (occurrences: 0-1).

**Allowed values, examples, other constraints**

Examples:

* http://www.isni.org
* http://orcid.org

.. _d:creator_affiliation:

2.3 affiliation (R)
~~~~~~~~~~~~~~~~~~~
The organizational or institutional affiliation of the creator (occurrences: 0-n).

**Allowed values, examples, other constraints**

Free text.

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <creators>
    <creator>
     <creatorName>Miller, John</creatorName>
    </creator>
    <creator>
     <creatorName>Smith, Jane</creatorName>
     <affiliation>OpenAIRE</affiliation>
     <nameIdentifier nameIdentifierScheme="ISNI"
                     schemeURI="http://www.isni.org">
      1422 4586 3573 0476
     </nameIdentifier>
    </creator>
   </creators>
