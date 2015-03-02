.. _d:relatedidentifier:

12. RelatedIdentifier (MA)
--------------------------

Identifiers of related resources. These must be globally unique identifiers (occurrences: 0-n).

**Allowed values, examples, other constraints**

Free text.

Use this property to indicate subsets of properties, as appropriate.

.. note::

   *Mandatory when applicable* property in OpenAIRE instead of *recommended* in DataCite.

   Please refer to :ref:`relations` for specific details on how to link datasets and publications.

.. _d:relatedidentifiertype:

12.1 relatedIdentifierType (M)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The type of the RelatedIdentifier (occurrences: 1).

**Allowed values, examples, other constraints**

If :ref:`d:relatedidentifier` is used, :ref:`d:relatedidentifiertype` is mandatory.

*Controlled List Values:*

* ``ARK``
* ``arXiv``
* ``bibcode``
* ``DOI``
* ``EAN13``
* ``EISSN``
* ``Handle``
* ``ISBN``
* ``ISSN``
* ``ISTC``
* ``LISSN``
* ``LSID``
* ``PMID``
* ``PURL``
* ``UPC``
* ``URL``
* ``URN``

.. _d:relationtype:

12.2 relationType (M)
~~~~~~~~~~~~~~~~~~~~~~

Description of the relationship of the resource being registered (A) and the related resource (B) (occurrences: 1).

**Allowed values, examples, other constraints**

If :ref:`d:relatedidentifier` is used, :ref:`d:relationtype` is mandatory.

*Controlled List Values:*

* ``IsCitedBy`` (indicates that B includes A in a citation)
* ``Cites`` (indicates that A includes B in a citation)
* ``IsSupplementTo`` (indicates that A is a supplement to B)
* ``IsSupplementedBy`` (indicates that B is a supplement to A)
* ``IsContinuedBy`` (indicates A is continued by the work B)
* ``Continues`` (indicates A is a continuation of the work B)
* ``HasMetadata`` (indicates resource A has additional metadata B)
* ``IsMetadataFor`` (indicates additional metadata A for a resource B)
* ``IsNewVersionOf`` (indicates A is a new edition of B, where the new edition has been modified or updated)
* ``IsPreviousVersionOf`` (indicates A is a previous edition of B)
* ``IsPartOf`` (indicates A is a portion of B;may be used for elements of a series)
* ``HasPart`` (indicates A includes the part B)
* ``IsReferencedBy`` (indicates A is used as a source of information by B)
* ``References`` (indicates B is used as a source of information for A)
* ``IsDocumentedBy`` (indicates B is documentation about/explaining A)
* ``Documents`` (indicates A is documentation about/explaining B)
* ``isCompiledBy`` (indicates B is used to compile or create A)
* ``Compiles`` (indicates B is the result of a compile or creation event using A)
* ``IsVariantFormOf`` (indicates A is a variant or different form of B, e.g. calculated or calibrated form or different packaging)
* ``IsOriginalFormOf`` (indicates A is the original form of B)
* ``IsIdenticalTo`` (indicates that A is identical to B, for use when there is a need to register two separate instances of the same resource)
* ``IsReviewedBy`` (indicates that A is reviewed by B)
* ``Reviews`` (indicates that A is a review of B)
* ``IsDerivedFrom`` (indicates B is a source upon which A is based)
* ``IsSourceOf`` (indicates A is a source upon which B is based)

.. note::

   ``Cites`` and ``IsCitedBy`` is specifically for when a publication/dataset directly cites another publication/dataset in its references, whereas ``References`` and ``IsReferencedBy`` is for when a dataset/publication is used as a source of information without a direct citation.

   OpenAIRE encourages including minimum one of above listed relation types, but allows usage of all DataCite’s relation types.


.. _d:relatedmetadatascheme:

12.3 relatedMetadataScheme (O)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The name of the scheme (occurrences: 0-1).

**Allowed values, examples, other constraints**

Use only with this relation pair: (``HasMetadata``/``IsMetadataFor``).

.. _d:relatedidentifier_schemuri:

12.1 schemeURI (O)
~~~~~~~~~~~~~~~~~~

The URI of the relatedMetadataScheme (occurrences: 0-1).

**Allowed values, examples, other constraints**

Use only with this relation pair: (``HasMetadata``/``IsMetadataFor``).

.. _d:relatedidentifier_schemeType:

12.1 schemeType (O)
~~~~~~~~~~~~~~~~~~~

The type of the relatedMetadataScheme, linked with the schemeURI (occurrences: 0-1).

**Allowed values, examples, other constraints**

Use only with this relation pair: (``HasMetadata``/``IsMetadataFor``).

Examples: ``XSD``, ``DDT``, ``Turtle``

Example
~~~~~~~

.. include:: examples/relatedidentifier.rst
